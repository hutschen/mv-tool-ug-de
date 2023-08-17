.. _catalogs:

####################
Anforderungskataloge
####################

Mit Hilfe von Anforderungskatalogen können Sie Anforderungen aus Standards und
Richtlinien zentral im MV-Tool verwalten und in verschiedenen Projekten
wiederverwenden. Die Anforderungskataloge sind hierarchisch aufgebaut. Die
oberste Ebene repräsentiert die Anforderungskataloge selbst. Diese enthalten
wiederum :ref:`Katalogmodule <modules>`, die ihrerseits
:ref:`Kataloganforderungen <requirements>` enthalten.

Um zu den Anforderungskatalogen zu gelangen, navigieren Sie über die
:ref:`navigation` zum Button :guilabel:`Catalogs`. Die Anforderungskataloge
werden nun in einer Tabelle dargestellt.

.. admonition:: Beispiel
  :class: note

  Ein typischer Anwendungsfall für Anforderungskataloge ist die Verwaltung der
  Anforderungen aus dem `IT-Grundschutz des BSI
  <https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/it-grundschutz_node.html>`_.
  Hierfür legen Sie zunächst einen :ref:`Anforderungskatalog <create_catalog>`
  an und nennen diesen zum Beispiel "IT-Grundschutz".

  Anschließend legen Sie für jeden Baustein des IT-Grundschutzes ein 
  :ref:`Modul <create_module>` im Anforderungskatalog an. Die Anforderungen aus
  den Bausteinen können Sie dann als :ref:`Kataloganforderungen <create_requirement>`
  in den Modulen anlegen.

  Die Anforderungen aus dem IT-Grundschutz müssen Sie nicht manuell übertragen,
  sondern können diese über die :ref:`Importfunktion <gs_import>` in den
  Anforderungskatalog importieren. Das Modul wird in diesem Fall automatisch
  angelegt.

.. _create_catalog:

Katalog anlegen
###############

Über der :ref:`Katalogtabelle <catalogs>` finden Sie den Button
:guilabel:`Create Catalog`. Klicken Sie auf diesen, um einen neuen Katalog
anzulegen. Es öffnet sich ein Dialog, in dem Sie die folgenden Datenfelder
ausfüllen können:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Reference`
     - Eine eindeutige Bezeichnung für den Katalog.
     - 
   * - :guilabel:`Title`
     - Ein aussagekräftiger Titel für den Katalog.
     - Ja
   * - :guilabel:`Description`
     - Eine optionale Beschreibung, die weitere Details über den Katalog enthält.
     - 

Bestätigen Sie Ihre Eingaben mit dem Button :guilabel:`Save`. Ihr neuer Katalog
wird nun in der :ref:`Katalogtabelle <catalogs>` angezeigt. 

.. note::

  Die Details der Kataloge können jederzeit über die :ref:`Eintrag-spezifischen
  Funktionen <eintrag-spezifische-funktionen>` bearbeitet werden.

.. _modules:

Katalogmodule
#############

Klicken Sie auf einen Katalog in der :ref:`Katalogtabelle <catalogs>`, um die
zugehörigen Katalogmodule in einer neuen Tabelle anzuzeigen. 

Katalogmodule sind eine Unterkategorie von Anforderungskatalogen. Sie
ermöglichen eine strukturierte Darstellung und effiziente Verwaltung der
Anforderungen innerhalb eines Katalogs.

.. _create_module:

Modul anlegen
=============

Über der :ref:`Modultabelle <modules>` finden Sie den Button :guilabel:`Create Module`. Klicken
Sie auf diesen, um ein neues Modul im aktuellen Katalog anzulegen. Es öffnet
sich ein Dialog, in dem Sie die folgenden Datenfelder ausfüllen können:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Reference`
     - Eine eindeutige Bezeichnung für das Modul.
     - 
   * - :guilabel:`Title`
     - Ein aussagekräftiger Titel für das Modul.
     - Ja
   * - :guilabel:`Description`
     - Eine optionale Beschreibung, die weitere Informationen über das Modul enthält.
     - 

Bestätigen Sie Ihre Eingaben mit dem Button :guilabel:`Save`. Ihr neues Modul
wird nun in der :ref:`Modultabelle <modules>` angezeigt.

.. note::

 Die Details der Module können jederzeit über die :ref:`Eintrag-spezifischen
 Funktionen <eintrag-spezifische-funktionen>` bearbeitet werden.

.. _requirements:

Kataloganforderungen
####################

Klicken Sie auf ein Modul in der :ref:`Modultabelle <modules>`, um die
zugehörigen Kataloganforderungen in einer neuen Tabelle anzuzeigen. 

Kataloganforderungen sind den Katalogmodulen untergeordnet und repräsentieren
die tatsächlichen Anforderungen aus den Standards.

.. _create_requirement:

Anforderung anlegen
===================

Über der :ref:`Anforderungstabelle <requirements>` finden Sie den Button
:guilabel:`Create Requirement`. Klicken Sie auf diesen, um eine neue Anforderung
im aktuellen Modul anzulegen. Es öffnet sich ein Dialog, in dem Sie die
folgenden Datenfelder ausfüllen können:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Reference`
     - Eine eindeutige Bezeichnung für die Anforderung.
     - 
   * - :guilabel:`Summary`
     - Eine prägnante Zusammenfassung der Anforderung.
     - Ja
   * - :guilabel:`Description`
     - Eine optionale Beschreibung, die weitere Informationen über die
       Anforderung liefert.
     - 

Bestätigen Sie Ihre Eingaben mit dem Button :guilabel:`Save`. Ihre neue
Anforderung wird nun in der :ref:`Anforderungstabelle <requirements>` angezeigt.

.. note::

  Die Details der Anforderungen können jederzeit über die
  :ref:`Eintrag-spezifischen Funktionen <eintrag-spezifische-funktionen>`
  bearbeitet werden.
