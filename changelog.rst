==========
Changelog
==========

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

.. _Server Version 0.11.1: https://github.com/hutschen/mv-tool-api/releases/tag/0.11.1
.. _Server Version 0.11.0: https://github.com/hutschen/mv-tool-api/releases/tag/0.11.0
.. _Client Version 0.11.0: https://github.com/hutschen/mv-tool-ng/releases/tag/0.11.0