#################
Import und Export
#################

Falls Sie bereits Anforderungen und Maßnahmen in Form von :ref:`Excel-Dateien
<excel_csv_import>` vorliegen haben, stellt dies kein Problem dar. Sie können diese
einfach in das MV-Tool importieren. Zudem können Sie Anforderungen aus
:ref:`IT-Grundschutz-Baussteinen <gs_import>` des IT-Grundschutz-Kompendiums
importieren.

Die Inhalte, die Sie im MV-Tool erstellt haben, können auch mit externen
Personen geteilt werden, die keinen Zugriff auf das MV-Tool haben. Hierfür
können Sie die Inhalte in eine :ref:`Excel-Datei exportieren <excel_csv_export>`.
Diese können Sie dann an die betreffende Person weitergeben. Wenn diese die
Inhalte bearbeitet hat, können Sie die Excel-Datei erneut in das MV-Tool
importieren und auf diese Weise die Änderungen übernehmen.

.. _import_gs_kompendium:

Import des IT-Grundschutz-Kompendiums
#####################################

.. hint::

  Bitte beachten Sie, dass bei der Verarbeitung von IT-Grundschutz-Bausteinen im
  MV-Tool die `Nutzungsbedingungen des BSI`_ einzuhalten sind.

Das MV-Tool ermöglicht den Import des IT-Grundschutz-Kompendiums im XML-Format.
Die entsprechende XML-Datei kann von der `Webseite zum IT-Grundschutz des BSI`_
heruntergeladen werden.

Um das IT-Grundschutz-Kompendium zu importieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Übersicht der :ref:`Anforderungskataloge <catalogs>`.
2. Klicken Sie auf den Button :guilabel:`Import` oberhalb der Tabelle. Ein
   Dropdown-Menü öffnet sich. Wählen Sie hier :menuselection:`Import from catalog` 
   und navigieren Sie im daraufhin erscheinenden Dialog zur XML-Datei.
   Bestätigen Sie den Import durch einen Klick auf :guilabel:`Upload file`.

.. _gs_import:

Import von IT-Grundschutz-Bausteinen
####################################

.. hint::

  Bitte beachten Sie, dass bei der Verarbeitung von IT-Grundschutz-Bausteinen im
  MV-Tool die `Nutzungsbedingungen des BSI`_ einzuhalten sind.

Sie können IT-Grundschutz-Baussteine des IT-Grundschutz-Kompendiums im
Word-Format in das MV-Tool importieren. Die Word-Dateien der Baussteine können
Sie auf der `Webseite zum IT-Grundschutz des BSI`_ herunterladen.

Sie haben auch die Möglichkeit,
:ref:`benutzerdefinierte IT-Grundschutz-Bausteine <gs_import_custom_bs>` zu
importieren, sofern diese als Word-Datei vorliegen und deren Struktur der
Struktur der Word-Dateien der IT-Grundschutz-Bausteine entspricht.

Folgen Sie diesen Schritten, um einen IT-Grundschutz-Baustein zu
importieren:

1. Legen Sie zunächst einen neuen :ref:`Anforderungskatalog <catalogs>` an und
   benennen Sie ihn entsprechend.
2. Öffnen Sie den Anforderungskatalog, indem Sie auf den Namen des
   Anforderungskatalogs in der Tabellenansicht klicken. Die
   :ref:`Tabelle mit den Modulen <modules>` des Anforderungskatalogs öffnet sich.
3. Klicken Sie auf den Button :guilabel:`Import` über der Modultabelle. Es
   öffnet sich ein Dropdown-Menü. Wählen Sie den Eintrag  :menuselection:`Import
   from catalog` aus. Wählen Sie im sich öffnenden Dialog die Word-Datei zum
   Upload aus und klicken Sie auf den Button :guilabel:`Upload file`.

Nach Abschluss des Uploads wird der IT-Grundschutz-Baustein in der
Modultabelle angezeigt. Durch Klicken auf den Namen des IT-Grundschutz-Bausteins
können Sie die Anforderungen des IT-Grundschutz-Bausteins in der
:ref:`Anforderungstabelle <requirements>` einsehen.

.. _Webseite zum IT-Grundschutz des BSI: https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html
.. _Nutzungsbedingungen des BSI: https://www.bsi.bund.de/DE/Service/Nutzungsbedingungen/Nutzungsbedingungen_node.html

.. _gs_import_custom_bs:

Import von benutzerdefinierten IT-Grundschutz-Bausteinen
========================================================

Neben den offiziellen IT-Grundschutz-Bausteinen des BSI können Sie über die
Import-Funktion für :ref:`IT-Grundschutz-Bausteine <gs_import>` auch eigene,
benutzerdefinierte Bausteine importieren. Voraussetzung ist, dass diese als
Word-Datei vorliegen und ihre Struktur derjenigen der IT-Grundschutz-Bausteine
entspricht.

Dokumentstruktur
----------------

Für die korrekte Verarbeitung im MV-Tool muss die Struktur des Word-Dokuments
wie folgt aussehen:

.. code-block:: none

  <Bausteintitel>
  └── <Überschrift_Anforderungen>
      ├── <Überschrift_B>
      │   ├── <Anforderungstitel>
      │   │   └── <Anforderungstext>
      │   └── ...
      ├── <Überschrift_S>
      │   ├── <Anforderungstitel>
      │   │   └── <Anforderungstext>
      │   └── ...
      └── <Überschrift_H>
          ├── <Anforderungstitel>
          │   └── <Anforderungstext>
          └── ...

Bitte verwenden Sie die Formatvorlagen von Word, um die oben dargestellte
Struktur umzusetzen. Welche Formatvorlagen für welche Elemente zu verwenden
sind, zeigt die folgende Tabelle:

.. list-table::
   :widths: 35 45 20
   :header-rows: 1

   * - Element
     - Inhalt
     - Formatvorlage
   * - ``<Bausteintitel>``
     - siehe :ref:`gs_import_custom_bs_title`
     - ``Titel``
   * - ``<Überschrift_Anforderungen>``
     - Text "Anforderungen"
     - ``Überschrift 1``
   * - ``<Überschrift_B>``
     - Text "Basis-Anforderungen"
     - ``Überschrift 2``
   * - ``<Überschrift_S>``
     - Text "Standard-Anforderungen"
     - ``Überschrift 2``
   * - ``<Überschrift_H>``
     - Text "Anforderungen bei erhöhtem Schutzbedarf"
     - ``Überschrift 2``
   * - ``<Anforderungstitel>``
     - siehe :ref:`gs_import_custom_bs_requirement_title`
     - ``Überschrift 3``
   * - ``<Anforderungstext>``
     - Beliebiger Text, der sich über mehrere Absätze erstrecken kann.
     - ``Fließtext``

.. _gs_import_custom_bs_title:

Auszeichnen des Bausteintitels
------------------------------

Formatieren Sie den Titel des Bausteins als Titel Ihres Word-Dokuments. In der
Regel finden Sie dafür eine vordefinierte Formatvorlage, die ``Überschrift 1`` 
übergeordnet ist. Der Titel Ihres Bausteins sollte wie folgt strukturiert sein:

.. code-block:: none

  <Baustein-ID> <Bausteinname>

.. list-table::
   :header-rows: 1

   * - Element
     - Beschreibung
     - Beispiel
     - Erforderlich
   * - ``<Baustein-ID>``
     - Beginnt mit einem oder mehreren Großbuchstaben, gefolgt von einer oder
       mehreren Zahlen, die durch Punkte getrennt sind.
     - ``B.1.2``
     - Ja
   * - ``<Bausteinname>``
     - Kann aus beliebigen Zeichen bestehen.
     - 
     - Ja

.. _gs_import_custom_bs_requirement_title:

Auszeichnen von Anforderungstiteln
----------------------------------

Die Anforderungstitel sollten den jeweiligen Überschriften zugeordnet und mit 
der Word-Formatvorlage ``Überschrift 3`` formatiert werden. Der Text der 
Anforderungen sollte mit der Formatvorlage ``Fließtext`` versehen werden.

Ein gültiger Anforderungstitel ist nach dem folgenden Schema aufgebaut. Dabei
darf die Reihenfolge der Elemente ``<Verantwortliche>`` und ``<Priorität>`` auch
vertauscht werden.

.. code-block:: none

  <Anforderungs-ID> <Anforderungsname> <Verantwortliche> <Priorität>

.. list-table::
   :header-rows: 1

   * - Element
     - Beschreibung
     - Beispiel
     - Erforderlich
   * - ``<Anforderungs-ID>``
     - Beginnt mit einem oder mehreren Großbuchstaben, gefolgt von einer oder
       mehreren Zahlen, die durch Punkte getrennt sind. Muss mit ``.A`` und
       einer oder mehreren Zahlen enden.
     - ``REQ.1.2.A1``
     - Ja
   * - ``<Anforderungsname>``
     - Kann aus beliebigen Zeichen bestehen.
     - 
     - Ja
   * - ``<Verantwortliche>``
     - Optional und in eckigen Klammern ``[ ]`` angegeben.
     - ``[Management]``
     - 
   * - ``<Priorität>``
     - Muss einer der folgenden Werte sein: ``B``, ``S`` oder ``H`` (für Basis-,
       Standard- oder Anforderungen bei erhöhtem Schutzbedarf). Angegeben in
       runden Klammern ``( )``.
     - ``(B)``
     - Ja


.. _excel_csv_import:

Excel- und CSV-Import
#####################

Sie können Anforderungen, Maßnahmen, Dokumente sowie Anforderungskataloge, deren
Module und Kataloganforderungen, die im Excel- oder CSV-Format vorliegen, in das
MV-Tool importieren. Dabei muss die Excel- oder CSV-Datei bestimmte
Spaltenbezeichnungen aufweisen, damit das MV-Tool den Inhalt korrekt importieren
kann. Die erwarteten Spaltenbezeichnungen sind in den folgenden Abschnitten
aufgelistet.

Sie haben die Möglichkeit, mehrere Inhalte, die in Beziehung zueinander stehen,
gemeinsam in einer Excel- oder CSV-Datei zu importieren. So können Sie
beispielsweise Anforderungen, Maßnahmen und Dokumente gleichzeitig mithilfe
einer Excel-Datei importieren.

Um eine Excel- oder CSV-Datei zu importieren, gehen Sie wie folgt vor:

1. Wechseln Sie zur gewünschten Tabellenansicht (z.B. :ref:`Anforderungen
   <anforderungen>` oder :ref:`Maßnahmen <massnahmen>`).
2. Über der Tabelle finden Sie den Button :guilabel:`Import`, der entweder
   direkt den Import-Dialog öffnet oder ein Dropdown-Menü mit verschiedenen
   Import-Optionen anzeigt. In letzterem Fall wählen Sie den Eintrag
   :menuselection:`Import Excel/CSV`.
3. Im sich öffnenden Dialog wählen Sie die zu importierende Datei aus. Falls Sie
   eine CSV-Datei auswählen, müssen Sie weitere 
   :ref:`Einstellungen zum Dateiformat <csv_settings>` vornehmen. Klicken Sie
   anschließend auf den Button :guilabel:`Upload file`, um den Import zu
   starten.

Nachdem der Upload abgeschlossen ist, werden die neu importierten Inhalte in der
Tabelle angezeigt.

.. _csv_settings:

Einstellungen für CSV-Dateien
=============================

Wenn Sie eine CSV-Datei importieren, müssen Sie weitere Einstellungen
vornehmen. Diese Einstellungen werden im Import- und Export-Dialog angezeigt,
sofern Sie CSV als Dateiformat ausgewählt haben.

Je nachdem, durch welches Programm Ihre CSV-Datei erstellt wurde, kann der
Aufbau variieren. CSV-Dateien können beispielsweise unterschiedliche
Zeichenkodierungen und Trennzeichen verwenden. Daher müssen Sie diese
Einstellungen vornehmen, um sicherzustellen, dass die CSV-Datei vom MV-Tool
korrekt gelesen oder geschrieben werden kann.

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Encoding`
     - Geben Sie hier die Zeichenkodierung der CSV-Datei an. Das MV-Tool bietet
       Ihnen eine Auswahl gängiger Zeichenkodierungen an. Sie können aber auch
       weitere, unkonventionellere Zeichenkodierungen angeben. Sofern die
       Zeichenkodierung nicht durch Ihre Instanz des MV-Tools unterstützt wird,
       wird beim Import eine Fehlermeldung angezeigt.
     - Ja
   * - :guilabel:`Delimiter`
     - Geben Sie hier das Trennzeichen an, das in der CSV-Datei verwendet wird.
       Gängige Trennzeichen sind beispielsweise Komma ``,`` oder Semikolon ``;``.
     - Ja

.. note::

  CSV-Dateien können sich zusätzlich zur Zeichenkodierung und zum Trennzeichen
  in anderen Punkten unterscheiden. Diese Formatunterschiede werden vom MV-Tool
  automatisch erkannt und berücksichtigt.

.. _project_columns:

Spaltenbezeichnungen von Projekten
==================================

Um Projektdaten aus einer Excel-Datei zu importieren, muss die Excel-Datei
bestimmte Spaltenbezeichnungen verwenden. Die Spaltenbezeichnungen, die das
MV-Tool für den Import von Projektdaten erwartet, sind nachfolgend aufgelistet.

.. list-table::
   :header-rows: 1

   * - Spaltenbezeichnung
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Project ID`
     - Wenn dieses Feld leer gelassen wird, wird ein neues Projekt im MV-Tool
       angelegt. Andernfalls wird das Projekt mit der angegebenen ID
       aktualisiert. Die IDs der Projekte erhalten Sie, wenn Sie diese aus dem
       MV-Tool exportieren.
     - 
   * - :guilabel:`Project Name`
     - Ein aussagekräftiger Name für das Projekt.
     - Ja
   * - :guilabel:`Project Description`
     - Eine optionale Beschreibung, die weitere Informationen über das Projekt liefert.
     - 
   * - :guilabel:`Jira Project Key`
     - Der Schlüssel bzw. die ID eines Jira-Projekts. Wenn diese angegeben ist,
       wird das Projekt mit dem Jira-Projekt verknüpft.
     - 


.. _requirement_columns:

Spaltenbezeichnungen von Anforderungen
======================================

Um Anforderungen aus einer Excel-Datei zu importieren, muss die Excel-Datei
bestimmte Spaltenbezeichnungen verwenden. Die Spaltenbezeichnungen, die das
MV-Tool für den Import von Anforderungen erwartet, sind nachfolgend aufgelistet.

.. list-table::
   :header-rows: 1

   * - Datenfeld
     - Beschreibung
     - Erforderlich
   * - :ref:`Kataloganforderung <catalog_requirement_columns>`
     - Sie können :ref:`catalog_requirement_columns` angeben, um die Anforderung
       mit einer Kataloganforderung zu verknüpfen.
     - 
   * - :ref:`Projekt <project_columns>`
     - Sie können :ref:`project_columns` angeben, um die Anforderung mit einem
       Projekt zu verknüpfen.
     - 
   * - :guilabel:`Requirement ID`
     - Wenn dieses Feld leer gelassen wird, wird eine neue Anforderung im
       MV-Tool angelegt. Andernfalls wird die Anforderung mit der angegebenen ID
       aktualisiert. Die IDs der Anforderungen erhalten Sie, wenn Sie diese aus
       dem MV-Tool exportieren.
     - 
   * - :guilabel:`Requirement Reference`
     - Ein Verweis oder eine Kennung zu der Anforderung.
     - 
   * - :guilabel:`Requirement Summary`
     - Eine prägnante Zusammenfassung der Anforderung.
     - Ja
   * - :guilabel:`Requirement Description`
     - Eine optionale Beschreibung, die weitere Informationen über die
       Anforderung liefert.
     - 
   * - :guilabel:`Requirement Compliance Status`
     - Der aktuelle :ref:`Erfüllungsgrad <compliance>` der Anforderung.
     - 
   * - :guilabel:`Requirement Compliance Comment`
     - Ein optionaler Kommentar zum :ref:`Erfüllungsgrad <compliance>` der
       Anforderung. Der Kommentarn kann nur angegeben werden, wenn der
       Erfüllungsgrad angegeben ist.
     - 
   * - :guilabel:`Requirement Target Object`
     - Das Zielobjekt der Anforderung, auf das sich die Anforderung bezieht.
     - 
   * - :guilabel:`Requirement Milestone`
     - Ein Meilenstein, der mit der Anforderung verknüpft ist.
     - 


.. _document_columns:

Spaltenbezeichnungen von Dokumenten
===================================

Um Dokumentendaten aus einer Excel-Datei zu importieren, muss die Excel-Datei
bestimmte Spaltenbezeichnungen verwenden. Die Spaltenbezeichnungen, die das
MV-Tool für den Import von Dokumentendaten erwartet, sind nachfolgend
aufgelistet.

.. list-table::
   :header-rows: 1

   * - Datenfeld
     - Beschreibung
     - Erforderlich
   * - :ref:`Projekt <project_columns>`
     - Sie können :ref:`project_columns` angeben, um das Dokument mit einem
       Projekt zu verknüpfen.
     - 
   * - :guilabel:`Document ID`
     - Wenn dieses Feld leer gelassen wird, wird ein neues Dokument im MV-Tool
       angelegt. Andernfalls wird das Dokument mit der angegebenen ID
       aktualisiert. Die IDs der Dokumente erhalten Sie, wenn Sie diese aus dem
       MV-Tool exportieren.
     - 
   * - :guilabel:`Document Reference`
     - Ein Verweis oder eine Kennung zu dem Dokument (z.B. eine
       Dokumentennummer).
     - 
   * - :guilabel:`Document Title`
     - Ein aussagekräftiger Titel für das Dokument.
     - Ja
   * - :guilabel:`Document Description`
     - Eine optionale Beschreibung, die weitere Informationen über das
       Dokument liefert.
     - 


.. _measure_columns:

Spaltenbezeichnungen von Maßnahmen
==================================

Um Maßnahmen aus einer Excel-Datei zu importieren, muss die Excel-Datei
bestimmte Spaltenbezeichnungen verwenden. Die Spaltenbezeichnungen, die das
MV-Tool für den Import von Maßnahmen erwartet, sind nachfolgend aufgelistet.

.. list-table::
   :header-rows: 1

   * - Datenfeld
     - Beschreibung
     - Erforderlich
   * - :ref:`Anforderung <requirement_columns>`
     - Sie können :ref:`requirement_columns` angeben, um die Maßnahme mit einer
       Anforderung zu verknüpfen.
     - 
   * - :guilabel:`Measure ID`
     - Wenn dieses Feld leer gelassen wird, wird eine neue Maßnahme im MV-Tool
       angelegt. Andernfalls wird die Maßnahme mit der angegebenen ID
       aktualisiert. Die IDs der Maßnahmen erhalten Sie, wenn Sie diese aus dem
       MV-Tool exportieren.
     - 
   * - :guilabel:`Measure Reference`
     - Ein Verweis oder eine Kennung zu der Maßnahme.
     - 
   * - :guilabel:`Measure Summary`
     - Eine prägnante Zusammenfassung der Maßnahme.
     - Ja
   * - :guilabel:`Measure Description`
     - Eine optionale Beschreibung, die weitere Informationen über die
       Maßnahme liefert.
     - 
   * - :ref:`Dokument <document_columns>`
     - Sie können :ref:`document_columns` angeben, um die Maßnahme mit einem
       Dokument zu verknüpfen.
     - 
   * - :guilabel:`Measure Compliance Status`
     - Der aktuelle :ref:`Erfüllungsgrad <compliance>` der Maßnahme.
     - 
   * - :guilabel:`Measure Compliance Comment`
     - Ein optionaler Kommentar zum :ref:`Erfüllungsgrad <compliance>` der
       Maßnahme.
     - 
   * - :guilabel:`Jira Issue Key`
     - Der Schlüssel bzw. die ID eines Jira-Issues. Wenn diese angegeben ist,
       wird die Maßnahme mit dem Jira-Issue verknüpft.
     - 
   * - :guilabel:`Measure Completion Status`
     - Der aktuelle :ref:`Umsetzungsstand <umsetzung>` der Maßnahme.
     - 
   * - :guilabel:`Measure Completion Comment`
     - Ein optionaler Kommentar zum :ref:`Umsetzungsstand <umsetzung>` der
       Maßnahme.
     - 
   * - :guilabel:`Measure Verification Method`
     - Die Methode, mit der die Umsetzung der Maßnahme :ref:`überprüft
       <verification>` wurde.
     - 
   * - :guilabel:`Measure Verification Status`
     - Der aktuelle Status der :ref:`Überprüfung <verification>` der Maßnahme.
     - 
   * - :guilabel:`Measure Verification Comment`
     - Ein optionaler Kommentar zum Status der :ref:`Überprüfung <verification>`
       der Maßnahme.
     - 

.. _catalog_columns:

Spaltenbezeichnungen von Anforderungskatalogen
==============================================

Um Anforderungskatalogdaten aus einer Excel-Datei zu importieren, muss die
Excel-Datei bestimmte Spaltenbezeichnungen verwenden. Die Spaltenbezeichnungen,
die das MV-Tool für den Import von Anforderungskatalogdaten erwartet, sind
nachfolgend aufgelistet.

.. list-table::
   :header-rows: 1

   * - Datenfeld
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Catalog ID`
     - Wenn dieses Feld leer gelassen wird, wird ein neuer Katalog im
       MV-Tool angelegt. Andernfalls wird der Katalog mit der angegebenen ID
       aktualisiert. Die IDs der Kataloge erhalten Sie, wenn Sie diese aus dem
       MV-Tool exportieren.
     - 
   * - :guilabel:`Catalog Reference`
     - Ein Verweis oder eine Kennung für den Katalog.
     - 
   * - :guilabel:`Catalog Title`
     - Ein aussagekräftiger Titel für den Katalog.
     - Ja
   * - :guilabel:`Catalog Description`
     - Eine optionale Beschreibung, die weitere Informationen über den Katalog
       liefert.
     - 


.. _module_columns:

Spaltenbezeichnungen von Modulen
================================

Um Moduldaten aus einer Excel-Datei zu importieren, muss die Excel-Datei
bestimmte Spaltenbezeichnungen verwenden. Die Spaltenbezeichnungen, die das
MV-Tool für den Import von Moduldaten erwartet, sind nachfolgend aufgelistet.

.. list-table::
   :header-rows: 1

   * - Datenfeld
     - Beschreibung
     - Erforderlich
   * - :ref:`Katalog <catalog_columns>`
     - Sie können :ref:`catalog_columns` angeben, um das Modul mit einem
       Katalog zu verknüpfen.
     - 
   * - :guilabel:`Catalog Module ID`
     - Wenn dieses Feld leer gelassen wird, wird ein neues Modul im
       MV-Tool angelegt. Andernfalls wird das Modul mit der angegebenen ID
       aktualisiert. Die IDs der Module erhalten Sie, wenn Sie diese aus dem
       MV-Tool exportieren.
     - 
   * - :guilabel:`Catalog Module Reference`
     - Ein Verweis oder eine Kennung für das Modul.
     - 
   * - :guilabel:`Catalog Module Title`
     - Ein aussagekräftiger Titel für das Modul.
     - Ja
   * - :guilabel:`Catalog Module Description`
     - Eine optionale Beschreibung, die weitere Informationen über das Modul liefert.
     - 


.. _catalog_requirement_columns:

Spaltenbezeichnungen von Kataloganforderungen
=============================================

Um Kataloganforderungen aus einer Excel-Datei zu importieren, muss die
Excel-Datei bestimmte Spaltenbezeichnungen verwenden. Die Spaltenbezeichnungen,
die das MV-Tool für den Import von Kataloganforderungen erwartet, sind
nachfolgend aufgelistet.

.. list-table::
   :header-rows: 1

   * - Datenfeld
     - Beschreibung
     - Erforderlich
   * - :ref:`Modul <module_columns>`
     - Sie können :ref:`module_columns` angeben, um die Kataloganforderung mit
       einem Modul zu verknüpfen.
     - 
   * - :guilabel:`Catalog Requirement ID`
     - Wenn dieses Feld leer gelassen wird, wird eine neue Kataloganforderung im
       MV-Tool angelegt. Andernfalls wird die Kataloganforderung mit der
       angegebenen ID aktualisiert. Die IDs der Kataloganforderungen erhalten
       Sie, wenn Sie diese aus dem MV-Tool exportieren.
     - 
   * - :guilabel:`Catalog Requirement Reference`
     - Ein Verweis oder eine Kennung für die Kataloganforderung.
     - 
   * - :guilabel:`Catalog Requirement Summary`
     - Eine prägnante Zusammenfassung der Kataloganforderung. Es handelt sich um
       ein optionales Feld.
     - 
   * - :guilabel:`Catalog Requirement Description`
     - Eine optionale Beschreibung, die weitere Informationen über die
       Kataloganforderung liefert.
     - 

.. _excel_csv_export:

Excel- und CSV-Export
#####################

Der Export von Inhalten aus dem MV-Tool in eine Excel- oder CSV-Datei ist in
allen Tabellenansichten möglich. Sie können beispielsweise Projektdaten,
Anforderungen, Maßnahmen, Dokumente, Anforderungskataloge, Module und
Kataloganforderungen exportieren.

Um Inhalte in eine Excel- oder CSV-Datei zu exportieren, folgen Sie bitte diesen
Schritten:

1. Klicken Sie auf den Button :guilabel:`Export` oberhalb der Tabelle.
   Wählen Sie im sich öffnenden Dialog die Spalten aus, die Sie exportieren
   möchten, und klicken Sie auf :guilabel:`Next`.
2. Im nächsten Schritt wählen Sie das gewünschte Dateiformat (Excel oder CSV)
   aus und geben Sie den gewünschten Dateinamen für die zu exportierende Datei ein.
   Falls Sie CSV als Dateiformat ausgewählt haben, müssen Sie weitere
   :ref:`Einstellungen zum Dateiformat <csv_settings>` vornehmen. Klicken Sie
   abschließend auf :guilabel:`Download`, um den Export zu starten.
3. Sobald der Downloadvorgang abgeschlossen ist, klicken Sie auf den Button
   :guilabel:`Save file`, um die heruntergeladene Datei zu speichern.

.. hint:

  Wenn Sie eine Excel- oder CSV-Datei exportieren, werden nur die Inhalte
  exportiert, die gerade in der Tabelle angezeigt werden. Wenn Sie also
  beispielsweise in der Tabelle :ref:`Anforderungen <anforderungen>` nach
  bestimmten Anforderungen suchen oder filtern, werden nur die resultierenden
  Anforderungen exportiert. Auch die Sortierung der Inhalte in der Tabelle wird
  beim Export berücksichtigt.

  Leere Spalten werden beim Export nicht berücksichtigt, auch wenn sie in der
  Auswahl der zu exportierenden Spalten enthalten sind.
