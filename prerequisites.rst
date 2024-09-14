=====================
Systemvoraussetzungen
=====================

Docker
======

Das MV-Tool ist eine Webanwendung, die in einem Docker-Container ausgeführt
wird. Demnach benötigen Sie für die Bereitstellung des MV-Tools einen Server,
auf dem Sie Docker-Container ausführen können. Sie müssen die Docker-Engine auf
Ihrem Server-System installieren. Die Installationsanweisungen dazu finden Sie
auf der `Website von Docker <https://docs.docker.com/engine/install/>`_.

.. TODO: Podman als Alternative zu Docker erwähnen.

Benutzerauthentifizierung
=========================

Das MV-Tool verfügt derzeit über keine eigene Benutzerverwaltung, sondern
verwendet für die Benutzerauthentifizierung einen externen :ref:`LDAP-Dienst
<connect_to_ldap>` oder die :ref:`JIRA-Instanz <connect_to_jira>`, mit der es
verbunden ist. Die Benutzer melden sich beim MV-Tool mit ihren LDAP- oder
JIRA-Anmeldedaten an.

Bei einer Authentifizierung über LDAP übermittelt das MV-Tool die Anmeldedaten
an den LDAP-Server, um die Anmeldung zu überprüfen. Bei der Authentifizierung
über JIRA verwendet das MV-Tool die Anmeldedaten des Benutzers, um sich über
HTTP Basic Auth bei der JSON-API der JIRA-Instanz zu authentifizieren. In beiden
Fällen werden die Anmeldedaten nicht serverseitig vom MV-Tool gespeichert und
das MV-Tool verwaltet keine serverseitigen Benutzersitzungen. Die
Benutzersitzung wird nur clientseitig, d.h. im Browser des Benutzers verwaltet. 

.. TODO: Auf eigener Seite die Sicherheit der Benutzerauthentifizierung erläutern und hier verlinken.

.. hint::

    Wenn Sie JIRA als Cloud-Service von Atlassian nutzen, können Sie HTTP Basic
    Auth nur eingeschränkt verwenden. Benutzer können sich dann am MV-Tool nicht
    mit ihrem normalen Benutzerpasswort anmelden, sondern müssen ein
    Zugriffstoken verwenden. Dieses Token müssen Sie zuvor in Ihrem
    JIRA-Benutzerprofil generieren. Weitere Informationen finden Sie in der
    `JIRA Dokumentation
    <https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account/>`_.

JIRA
====

Wenn Sie JIRA-Tickets mit Maßnahmen im MV-Tool verknüpfen möchten, ist eine
Verbindung zu JIRA erforderlich. Dazu benötigen Sie eine JIRA-Instanz mit
aktivierter JSON-API, auf die das MV-Tool über HTTP/HTTPS zugreifen kann. Die
JSON API ist in JIRA standardmäßig aktiviert.

.. note::

   Das MV-Tool wird mit JIRA Version 9 getestet. Das MV-Tool verwendet `jira-python
   <https://jira.readthedocs.io/>`_ für den Zugriff auf JIRA. Eine
   Kompatibilität mit früheren JIRA Versionen kann daher gegeben sein.

Datenbank
=========

Derzeit werden SQLite und PostgreSQL als Datenbanken unterstützt. Wenn Sie das
MV-Tool im Produktivbetrieb einsetzen möchten, sollten Sie PostgreSQL verwenden.
SQLite sollte nicht für den Produktiveinsatz verwendet werden, da seine
Reaktionszeiten mit SQLite deutlich geringer sind, als mit PostgreSQL.

SQLite
------

SQLite ist eine gute Wahl für Testumgebungen, da es keine zusätzliche
Datenbank-Software erfordert. Wenn Sie SQLite verwenden möchten, müssen Sie also
nichts weiter tun und können mit der :ref:`Installation <installation>`
fortfahren.

PostgreSQL
----------

PostgreSQL ist die empfohlene Datenbank für den Produktivbetrieb. Um PostgreSQL
zu nutzen, müssen Sie eine PostgreSQL-Datenbank auf Ihrem Server installieren
und bereitstellen. Anweisungen zur Installation von PostgreSQL finden Sie auf
der `Website von PostgreSQL <https://www.postgresql.org/download/>`_.

.. note::

   Das MV-Tool wird mit PostgreSQL Version 14 und 15 getestet.