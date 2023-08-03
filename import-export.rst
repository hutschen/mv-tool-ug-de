#################
Import und Export
#################

Falls Sie bereits Anforderungen und Maßnahmen in Form von :ref:`Excel-Dateien
<excel_import>` vorliegen haben, stellt dies kein Problem dar. Sie können diese
einfach in das MV-Tool importieren. Zudem können Sie Anforderungen aus
:ref:`IT-Grundschutz-Baussteinen <gs_import>` des IT-Grundschutz-Kompendiums
importieren.

Die Inhalte, die Sie im MV-Tool erstellt haben, können auch mit externen
Personen geteilt werden, die keinen Zugriff auf das MV-Tool haben. Hierfür
können Sie die Inhalte in eine :ref:`Excel-Datei exportieren <excel_export>`.
Diese können Sie dann an die betreffende Person weitergeben. Wenn diese die
Inhalte bearbeitet hat, können Sie die Excel-Datei erneut in das MV-Tool
importieren und auf diese Weise die Änderungen übernehmen.

.. _gs_import:

Import von IT-Grundschutz Bausteinen
####################################

Sie können IT-Grundschutz-Baussteine des IT-Grundschutz-Kompendiums im
Word-Format in das MV-Tool importieren. Die Word-Dateien der
IT-Grundschutz-Baussteine können Sie auf der `Webseite des BSI herunterladen
<https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/IT-Grundschutz-Bausteine/Bausteine_Download_Edition_node.html>`_.

Sie haben ebenso die Möglichkeit, benutzerdefinierte IT-Grundschutz-Bausteine zu importieren,
sofern diese als Word-Datei vorliegen und deren Struktur der
Struktur der Word-Dateien der IT-Grundschutz-Bausteine entspricht.

.. hint::

  Bitte beachten Sie, dass bei der Verarbeitung von
  IT-Grundschutz-Bausteinen im MV-Tool die `Nutzungsbedingungen des BSI
  <https://www.bsi.bund.de/DE/Service/Nutzungsbedingungen/Nutzungsbedingungen_node.html>`_
  einzuhalten sind.

Folgen Sie diesen Schritten, um einen IT-Grundschutz-Baustein zu
importieren:

1. Legen Sie zunächst einen neuen :ref:`Anforderungskatalog <catalogs>` an und
   benennen Sie ihn entsprechend.
2. Öffnen Sie den Anforderungskatalog, indem Sie auf den Namen des
   Anforderungskatalogs in der Tabellenansicht klicken. Die
   :ref:`Tabelle mit den Modulen <modules>` des Anforderungskatalogs öffnet sich.
3. Klicken Sie auf den Button :guilabel:`Import` über der Modultabelle. Es
   öffnet sich ein Dropdown-Menü. Wählen Sie den Eintrag  :menuselection:`Import
   from catalog` aus. Wählen Sie im sich öffnenden Dialog den
   IT-Grundschutz-Baustein zum Upload aus und klicken Sie auf den Button
   :guilabel:`Upload file`.

Nach Abschluss des Uploads wird der IT-Grundschutz-Baustein in der
Modultabelle angezeigt. Durch Klicken auf den Namen des IT-Grundschutz-Bausteins
können Sie die Anforderungen des IT-Grundschutz-Bausteins in der
:ref:`Anforderungstabelle <requirements>` einsehen.

.. _excel_import:

Import aus einer Excel-Datei
############################

Sie können Anforderungen, Maßnahmen, Dokumente sowie Anforderungskataloge und
deren Module aus Excel-Dateien in das MV-Tool importieren. Dabei muss die
Excel-Datei bestimmte Spaltenbezeichnungen aufweisen, damit das MV-Tool den
Inhalt korrekt importieren kann. Die erwarteten Spaltenbezeichnungen sind in den
folgenden Abschnitten aufgelistet.

Sie haben die Möglichkeit, mehrere Inhalte, die in Beziehung zueinander stehen,
gemeinsam in einer Excel-Datei zu importieren. So können Sie beispielsweise
Anforderungen, Maßnahmen und Dokumente gleichzeitig mithilfe einer Excel-Datei
importieren.

Um eine Excel-Datei zu importieren, gehen Sie wie folgt vor:

1. Wechseln Sie zur gewünschten Tabellenansicht (z.B. :ref:`Anforderungen
   <anforderungen>` oder :ref:`Maßnahmen <massnahmen>`).
2. Über der Tabelle finden Sie entweder den Button :guilabel:`Import Excel` oder
   den Button :guilabel:`Import`, der ein Dropdown-Menü mit verschiedenen
   Import-Optionen öffnet. In letzterem Fall wählen Sie den Eintrag
   :menuselection:`Import from Excel`.
3. Im sich öffnenden Dialog wählen Sie die zu importierende Excel-Datei aus und
   klicken Sie auf den Button :guilabel:`Upload file`.

Nachdem der Upload abgeschlossen ist, werden die neu importierten Inhalte in der
Tabelle angezeigt.

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

.. _excel_export:

Export in eine Excel-Datei
##########################

Der Export von Inhalten aus dem MV-Tool in eine Excel-Datei ist in allen
Tabellenansichten möglich. So lassen sich beispielsweise Projektdaten,
Anforderungen, Maßnahmen, Dokumente, Anforderungskataloge, Module und
Kataloganforderungen exportieren.

Um eine Excel-Datei zu exportieren, folgen Sie bitte diesen Schritten:

1. Klicken Sie auf den Button :guilabel:`Export Excel` oberhalb der Tabelle.
   Wählen Sie im sich öffnenden Dialog die Spalten aus, die Sie exportieren
   möchten, und klicken Sie auf :guilabel:`Next`.
2. Geben Sie im nächsten Schritt den gewünschten Dateinamen für die zu
   exportierende Excel-Datei ein und klicken Sie auf :guilabel:`Download`.
3. Sobald der Downloadvorgang abgeschlossen ist, klicken Sie auf den Button
   :guilabel:`Save file`, um die heruntergeladene Datei zu speichern.

.. hint:

  Wenn Sie eine Excel-Datei exportieren, werden nur die Inhalte exportiert, die
  gerade in der Tabelle angezeigt werden. Wenn Sie also beispielsweise in der
  Tabelle :ref:`Anforderungen <anforderungen>` nach bestimmten Anforderungen
  filtern oder suchen, werden nur die resultierenden Anforderungen exportiert.
  Auch die Sortierung der Inhalte in der Tabelle wird beim Export
  berücksichtigt.

  Leere Spalten werden beim Export nicht berücksichtigt, auch wenn sie in der
  Auswahl der zu exportierenden Spalten enthalten sind.

