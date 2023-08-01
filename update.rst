##############
Aktualisierung
##############

Das Aktualisieren (Upgrade) und Herabstufen (Downgrade) von Versionen des
MV-Tools ist problemlos möglich.

Folgen Sie diesen Schritten, um Ihr MV-Tool zu aktualisieren:

1. Sichern Sie zunächst Ihre Datenbank und die Konfigurationsdatei `config.yml`,
   um einen Datenverlust zu vermeiden.
2. Laden Sie anschließend das Docker-Image der gewünschten Version herunter oder
   erstellen Sie es selbst (siehe :ref:`docker-image-bauen`).
3. Stoppen Sie schließlich den laufenden Container und starten Sie ihn mit dem
   neuen Image neu.

Wenn die aktualisierte Version des MV-Tools gestartet wird, wird Ihre Datenbank
automatisch auf den neuesten Stand gebracht. Eine manuelle Migration ist hierbei
nicht erforderlich.

.. warning::

    Bitte beachten Sie, dass beim Downgrade auf eine ältere Version des MV-Tools
    Datenverluste auftreten können. Dies liegt daran, dass bestimmte
    Datenbankfelder oder -tabellen in der älteren Version möglicherweise nicht
    existieren. Aus diesem Grund ist dringend empfohlen, vor einem Downgrade
    immer ein Backup der Datenbank zu erstellen.
