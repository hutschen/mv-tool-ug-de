==========
Changelog
==========

Version 0.15.0
==============

Veröffentlicht am 15.11.2023. Bestehend aus `Server Version 0.15.0`_ und 
`Client Version 0.15.0`_.

.. list-table::
   :header-rows: 1

   * - Typ
     - Part
     - Beschreibung
     - Issue
   * - Enhancement
     - Server, Client
     - Einführung eines neuen Features zum 
       :ref:`Import von Katalogen <import_gs_kompendium>`, deren Modulen und
       Anforderungen im XML-Format. Der Server wurde um eine neue
       Web-API-Schnittstelle erweitert, um den Upload der XML-Dateien zu
       ermöglichen. Die UI des Clients wurde um eine Funktion für den Upload
       einer XML-Datei erweitert.
     - `#157 <https://github.com/hutschen/mv-tool-api/issues/157>`_,
       `#134 <https://github.com/hutschen/mv-tool-ng/issues/134>`_

Version 0.14.2
==============

Veröffentlicht am 14.11.2023. Bestehend aus `Server Version 0.14.2`_ und 
`Client Version 0.14.0`_.

.. list-table::
   :header-rows: 1

   * - Typ
     - Part
     - Beschreibung
     - Issue
   * - Bugfix
     - Server
     - Behebung eines Fehlers im Zusammenhang mit dem
       ``verify_ssl``-Konfigurationsparameter bei der Verwendung von
       LDAPS-Verbindungen zu einem LDAP-Verzeichnisdienst.
     - `#171 <https://github.com/hutschen/mv-tool-api/issues/171>`_

Version 0.14.1
==============

Veröffentlicht am 12.10.2023. Bestehend aus `Server Version 0.14.1`_ und 
`Client Version 0.14.0`_.

.. list-table::
   :header-rows: 1

   * - Typ
     - Part
     - Beschreibung
     - Issue
   * - Enhancement
     - Server
     - Die :ref:`Anbindung an einen LDAP-Verzeichnisdienst <connect_to_ldap>`
       ist nun möglich, so dass sich Benutzer mit ihren LDAP-Zugangsdaten
       anmelden können.
     - `#159 <https://github.com/hutschen/mv-tool-api/issues/159>`_

Version 0.14.0
==============

Veröffentlicht am 30.09.2023. Bestehend aus `Server Version 0.14.0`_ und 
`Client Version 0.14.0`_.

.. list-table::
   :header-rows: 1

   * - Typ
     - Part
     - Beschreibung
     - Issue
   * - Enhancement
     - Server, Client
     - Im Client können nun JIRA-Benutzer als Bearbeiter beim 
       :ref:`Erstellen von Tickets <create_issue>` ausgewählt werden. Im Server
       wurden dazu neue Web-API-Endpunkte zu Abfrage von JIRA-Benutzern
       hinzugefügt und Anpassungen am Datenmodell vorgenommen.
     - `#158 <https://github.com/hutschen/mv-tool-api/issues/158>`_, 
       `#160 <https://github.com/hutschen/mv-tool-api/issues/160>`_,
       `#127 <https://github.com/hutschen/mv-tool-ng/issues/127>`_
   * - Enhancement
     - Client
     - Überarbeitung des Upload-Dialogs zur Verwendung der gleichen Komponenten
       wie im Import-Dialog für Excel und CSV-Dateien.
     - `#122 <https://github.com/hutschen/mv-tool-ng/issues/122>`_


Version 0.13.0
==============

Veröffentlicht am 10.09.2023. Bestehend aus `Server Version 0.13.0`_ und 
`Client Version 0.13.0`_.

.. list-table::
   :header-rows: 1

   * - Typ
     - Part
     - Beschreibung
     - Issue
   * - Enhancement
     - Server, Client
     - :ref:`Import <excel_csv_import>` und :ref:`Export <excel_csv_export>` von
       Projekten, Anforderungen, Maßnahmen, Dokumenten, Katalogen,
       Katalogmodulen und Kataloganforderungen im CSV-Format.
     - `#142 <https://github.com/hutschen/mv-tool-api/issues/142>`_,
       `#119 <https://github.com/hutschen/mv-tool-ng/issues/119>`_,

Version 0.12.0
==============

Veröffentlicht am 27.08.2023. Bestehend aus `Server Version 0.12.0`_ und 
`Client Version 0.12.0`_.

.. list-table::
   :header-rows: 1

   * - Typ
     - Part
     - Beschreibung
     - Issue
   * - Enhancement
     - Server, Client
     - Wenn der :ref:`Erfüllungsgrad <compliance>` einer Anforderung nicht mit
       dem Erfüllungsgrad der zugehörigen Maßnahmen übereinstimmt, wird in der
       UI ein Hinweis angezeigt. Das Filtern und Sortieren nach diesen Hinweisen
       ist nun möglich.
     - `#153 <https://github.com/hutschen/mv-tool-api/issues/153>`_,
       `#112 <https://github.com/hutschen/mv-tool-ng/issues/112>`_
   * - Enhancement
     - Server, Client
     - Der Web-API-Endpunkt zur Abfrage von JIRA-Tickets wurde überarbeitet, um
       Tickets paginiert und gefiltert abfragen zu können. In der UI wurde
       Auswahldialog für JIRA-Tickets überarbeitet, so dass nur Tickets vom
       Server abgefragt werden, die als Vorschlag zur Auswahl angezeigt werden
       sollen.
     - `#154 <https://github.com/hutschen/mv-tool-api/issues/154>`_,
       `#113 <https://github.com/hutschen/mv-tool-ng/issues/113>`_,
   * - Bugfix
     - Server
     - Behebt einen Fehler bei der Behandlung von JIRA-Fehlern.
     - `#155 <https://github.com/hutschen/mv-tool-api/issues/155>`_
   * - Enhancement
     - Client
     - Es wurden die Funktionen zur Auswahl und Bearbeitung von JIRA-Tickets
       überarbeitet, die Maßnahmen zugeordnet sind überarbeitet.
     - `#114 <https://github.com/hutschen/mv-tool-ng/issues/114>`_
   * - Enhancement
     - Client
     - Änderungen, die am Erfüllungsgrad, am Umsetzungsstatus, der
       Überprüfungsmethode oder dem Überprüfungsstatus einer Maßnahme
       vorgenommen werden, werden nun effizienter per `PATCH`-Request an den
       Server gesendet.
     - `#116 <https://github.com/hutschen/mv-tool-ng/issues/116>`_,
   * - Enhancement
     - Server, Client
     - Referenzen von Anforderungen, Maßnahmen, Dokumenten, Katalogmodulen und
       Kataloganforderungen können nun 
       :ref:`automatisch nummeriert <bulk_edit_numbering>` werden.
     - `#117 <https://github.com/hutschen/mv-tool-ng/issues/117>`_,
       `#156 <https://github.com/hutschen/mv-tool-api/issues/156>`_

Version 0.11.1
==============

Veröffentlicht am 28.07.2023. Bestehend aus `Server Version 0.11.1`_ und 
`Client Version 0.11.0`_.

.. list-table::
   :header-rows: 1

   * - Typ
     - Part
     - Beschreibung
     - Issue
   * - Bugfix
     - Server
     - Beschleunigung der Abfrage von Spalten bzw. Feldbezeichnungen, die in
       Projekten, Anforderungen, Maßnahmen etc. verwendet werden.
     - `#152 <https://github.com/hutschen/mv-tool-api/issues/152>`_

Version 0.11.0
==============

Veröffentlicht am 26.07.2023. Bestehend aus `Server Version 0.11.0`_ und 
`Client Version 0.11.0`_.

.. list-table::
   :header-rows: 1

   * - Typ
     - Part
     - Beschreibung
     - Issue
   * - Enhancement
     - Client
     - Der Fortschritt der Abarbeitung von Maßnahmen wird detailierter angezeigt. Neben dem prozentualen Fortschritt werden die Anzahl der zu erledigenden und erledigten Maßnahmen angezeigt.
     - `#110 <https://github.com/hutschen/mv-tool-ng/issues/110>`_
   * - Enhancement
     - Server
     - Hinzufügen von Fortschrittsdaten zu Projekten, Anforderungen und Dokumenten aus denen der Client den Arbeitsfortschritt berechnen kann.
     - `#151 <https://github.com/hutschen/mv-tool-api/issues/151>`_
   * - Verbesserung
     - Server
     - Aktualisierung der Abhängigkeit zu ``pydantic`` auf Version 2.0 und Migration des Codes auf die neue Version.
     - `#149 <https://github.com/hutschen/mv-tool-api/issues/149>`_
   * - Verbesserung
     - Server
     - Aktualisierung der Abhängigkeit zu ``sqlalchemy`` auf Version 2.0 und Migration des Codes auf die neue Version.
     - `#145 <https://github.com/hutschen/mv-tool-api/issues/145>`_

----------

Frühere Versionen
=================

Das Changelog für frühere Versionen kann auf GitHub eingesehen werden. Dies gilt
sowohl für den `Server <https://github.com/hutschen/mv-tool-api/releases>`_ als
auch für den `Client <https://github.com/hutschen/mv-tool-ng/releases>`_ des
MV-Tools.

.. _Server Version 0.15.0: https://github.com/hutschen/mv-tool-api/releases/tag/0.15.0
.. _Client Version 0.15.0: https://github.com/hutschen/mv-tool-ng/releases/tag/0.15.0
.. _Server Version 0.14.2: https://github.com/hutschen/mv-tool-api/releases/tag/0.14.2
.. _Server Version 0.14.1: https://github.com/hutschen/mv-tool-api/releases/tag/0.14.1
.. _Server Version 0.14.0: https://github.com/hutschen/mv-tool-api/releases/tag/0.14.0
.. _Server Version 0.13.0: https://github.com/hutschen/mv-tool-api/releases/tag/0.13.0
.. _Server Version 0.12.0: https://github.com/hutschen/mv-tool-api/releases/tag/0.12.0
.. _Server Version 0.11.1: https://github.com/hutschen/mv-tool-api/releases/tag/0.11.1
.. _Server Version 0.11.0: https://github.com/hutschen/mv-tool-api/releases/tag/0.11.0
.. _Client Version 0.14.0: https://github.com/hutschen/mv-tool-ng/releases/tag/0.14.0
.. _Client Version 0.13.0: https://github.com/hutschen/mv-tool-ng/releases/tag/0.13.0
.. _Client Version 0.12.0: https://github.com/hutschen/mv-tool-ng/releases/tag/0.12.0
.. _Client Version 0.11.0: https://github.com/hutschen/mv-tool-ng/releases/tag/0.11.0