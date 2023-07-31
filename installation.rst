.. _installation:

============
Installation
============

Die Installation des MV-Tools ist recht einfach, besonders wenn Ihr Server die
`AMD64-Architektur <https://de.wikipedia.org/wiki/AMD64>`_ verwendet. In diesem
Fall können Sie das Docker-Image direkt von `Docker Hub
<https://hub.docker.com/r/hutschen/mv-tool>`_ herunterladen. Wenn Ihr System
jedoch eine andere Architektur verwendet, müssen Sie das Docker-Image selbst
erstellen. Weitere Informationen finden Sie im Abschnitt
:ref:`docker-image-bauen`.

.. code-block:: bash

    docker pull hutschen/mv-tool:latest

.. _docker-image-bauen:

Erstellen des Docker-Images
============================

Zuerst sollten Sie das Repository klonen, welches das Dockerfile enthält, das
zur Erstellung des Docker-Images verwendet wird. Bitte beachten Sie, dass dieses
Repository Submodule enthält, die zusammen mit dem Hauptrepository geklont
werden sollten. Dies erreichen Sie mit folgendem Befehl:

.. code-block:: bash

    git clone --recurse-submodules git@github.com:hutschen/mv-tool-docker.git

Stellen Sie sicher, dass `Docker <https://www.docker.com/>`_ auf Ihrem System
installiert ist. Wechseln Sie in das Hauptverzeichnis des Repositories und
führen Sie den folgenden Befehl aus, um das Docker-Image zu erstellen:

.. code-block:: bash

    docker image build -t hutschen/mv-tool .

Erstellen der Konfigurationsdatei
=================================

Bevor Sie das MV-Tool in einem Docker-Container ausführen können, ist eine
Konfiguration erforderlich. Dazu wird eine Konfigurationsdatei benötigt. Für die
minimale Konfiguration können Sie den folgenden Inhalt in eine Datei namens
``config.yml`` schreiben:

.. code-block:: yaml

    jira:
      url: http://localhost:2990/jira
    database:
      url: sqlite:///mvtool.db

.. admonition:: Info

    Ersetzen Sie bitte ``http://localhost:2990/jira`` durch die URL Ihrer
    JIRA-Instanz.

Verbindung zu JIRA herstellen
=============================

Um eine Verbindung zu JIRA herzustellen, geben Sie die URL Ihrer JIRA-Instanz in
der Datei ``config.yml`` ein.

.. admonition:: Info

    Es kann nötig sein, ``/jira`` an das Ende der URL anzuhängen. Falls Probleme
    bei der initialen Verbindung auftreten, versuchen Sie es mit dem Anhängen
    von ``/jira`` an die URL.

HTTPS/SSL
---------

Wenn Ihre JIRA-Instanz ein selbstsigniertes Zertifikat verwendet und Sie eine
HTTPS-Verbindung zu JIRA verwenden möchten, dann müssen Sie in der
Konfigurationsdatei ``config.yml`` zusätzlich zur URL auch die Option
``verify_ssl`` hinzufügen. Diese Option muss im ``jira``-Abschnitt der Datei
hinzugefügt und auf ``false`` gesetzt werden.


Datenbankverbindung herstellen
==============================

Das MV-Tool unterstützt SQLite und PostgreSQL als Datenbanken. Für den
produktiven Einsatz wird PostgreSQL empfohlen. In der ``config.yml``-Datei geben
Sie die URL zu Ihrer Datenbank ein.

SQLite
------

Die folgende Konfiguration zeigt, wie eine Verbindung zu einer SQLite-Datenbank
hergestellt wird:

.. code-block:: yaml

    database:
      url: sqlite:///mvtool.db

Die Datenbankdatei ``mvtool.db`` wird automatisch erstellt, wenn sie nicht
vorhanden ist.

.. admonition:: Info

    Das MV-Tool verwendet SQLAlchemy für die Datenbankverbindung. Daher muss die
    Datenbank-URL dem SQLAlchemy-Format entsprechen. Zusätzliche Informationen
    zur SQLite-Datenbank-URL finden Sie in der `SQLAlchemy Dokumentation
    <https://docs.sqlalchemy.org/en/14/dialects/sqlite.html#connect-strings>`_.

PostgreSQL
----------

Die folgende Konfiguration zeigt, wie eine Verbindung zu einer
PostgreSQL-Datenbank hergestellt wird:

.. code-block:: yaml

    database:
      url: postgresql+psycopg2://user:password@localhost:5432/mvtool

.. admonition:: Info

    Für Verbindungen zu PostgreSQL-Datenbanken wird der Treiber `psycopg2
    <https://www.psycopg.org/>`_ verwendet. Zusätzliche Informationen zur
    PostgreSQL-Datenbank-URL finden Sie in der `SQLAlchemy Dokumentation
    <https://docs.sqlalchemy.org/en/14/dialects/postgresql.html#dialect-postgresql-psycopg2-connect>`_.

Logging
=======

.. admonition:: Info

    Die Logging-Konfiguration ist optional. Wenn Sie keine Logging-Konfiguration
    benötigen, können Sie diesen Abschnitt überspringen oder direkt zum
    Abschnitt :ref:`docker-container-starten` springen.


Das Logging dient zur Identifizierung möglicher Fehler im MV-Tool, die in
zukünftigen Versionen behoben werden können. Sie können die Logs entweder direkt
über den Befehl ``docker logs`` abrufen oder Sie speichern diese in einer Datei
innerhalb des Docker-Containers.

Einstellen des Log-Levels
-------------------------

Der Log-Level bestimmt, welche Arten von Meldungen protokolliert werden. Es
stehen die Werte ``debug``, ``info``, ``warning``, ``error`` und ``critical``
zur Verfügung. Wenn Sie den Log-Level auf ``error`` setzen, werden zum Beispiel
alle Meldungen mit dem Log-Level ``error`` und ``critical`` protokolliert. Das
voreingestellte Log-Level ist ``error``.

.. code-block:: yaml

    uvicorn:
      log_level: error

Verwenden einer Log-Datei
-------------------------

Wenn Sie möchten können Sie die Log-Nachrichten in eine Datei schreiben. Dazu
müssen Sie den ``log_filename`` Parameter in der ``config.yml``-Datei
hinzufügen.

.. code-block:: yaml

    uvicorn:
      log_level: error
      log_filename: mvtool.log

Der Log-Dateiname (zum Beispiel ``mvtool.log``) legt den Namen der Datei fest,
in die die Log-Nachrichten geschrieben werden. Die Datei wird innerhalb des
Docker-Containers unter dem Pfad ``/usr/src/api/`` erzeugt und die Log-Einträge
werden an eine bestehende Datei angehängt. 

Um Zugriff auf die Log-Datei auch außerhalb des Containers zu erhalten, muss ein
Bind-Mount zwischen dem Host-System und dem Docker-Container erstellt werden. 

Erstellen Sie zunächst eine leere Log-Datei auf dem Host-System und binden Sie
diese beim Start des Docker-Containers mittels des ``-v`` Parameters des
``docker container create`` Befehls ein. Achten Sie darauf, dass der Pfad zur
Log-Datei auf dem Host-System und der Pfad im Docker-Container übereinstimmen
und dass der Docker-Container Schreibrechte auf die Datei hat.

.. code-block:: bash

    touch mvtool.log
    docker container create --name mv-tool -p 4200:8000 -v mvtool.log:/usr/src/api/mvtool.log hutschen/mv-tool

Secret für Authentifizierungs-Token
===================================

.. admonition:: Info

    Die Definition eines eigenen Secrets ist optional. Wenn Sie dies nicht
    wünschen, können Sie diesen Abschnitt überspringen oder direkt zum Abschnitt
    :ref:`docker-container-starten` springen.

Das MV-Tool nutzt Authentifizierungs-Token zur sicheren Speicherung von
Nutzersitzungen im Browser des Nutzers. Um diese Token zu erstellen, wird ein
Secret benötigt, welches das MV-Tool standardmäßig bei jedem Start neu
generiert. Dies führt allerdings dazu, dass alle bestehenden Nutzersitzungen bei
einem Neustart des MV-Tools ungültig werden.

Um diese Ungültigkeit zu verhindern, können Sie ein festes, eigenes Secret
einsetzen, welches sich bei Neustarts des MV-Tools nicht ändert. 

Um ein eigenes Secret in der ``config.yml``-Datei zu verwenden, geben Sie dieses
im Abschnitt ``auth`` wie folgt an:

.. code-block:: yaml

    auth:
      secret: "my-secret"

Sie können ein solches Secret mit folgendem Befehl generieren, falls ``openssl``
auf Ihrem System installiert ist:

.. code-block:: bash

    openssl rand -hex 32

Falls ``openssl`` nicht auf Ihrem System installiert ist, können Sie auch einen 
beliebigen Passwort-Generator verwenden. Wichtig ist nur, dass das Secret eine
Mindestlänge von 32 Byte hat und zufällig generiert wurde.

.. _docker-container-starten:

Start des Docker-Containers
===========================

Nach der Konfiguration können Sie den Docker-Container starten. Dabei kopieren
Sie die Konfigurationsdatei vor dem Start in den Container. Das folgende
Kommando startet den Docker-Container:

.. code-block:: bash

    docker container create --name mv-tool -p 4200:8000 hutschen/mv-tool
    docker container cp config.yml mv-tool:/usr/src/api/config.yml
    docker container start mv-tool

Der Docker-Container ist dann unter http://localhost:4200 erreichbar.
