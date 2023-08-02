.. _projects:

########
Projekte
########

Um mit dem MV-Tool zu arbeiten, müssen Sie zunächst ein Projekt anlegen. Ein
Projekt enthält eine Sammlung von :ref:`Anforderungen <anforderungen>`, denen
:ref:`Maßnahmen <massnahmen>` zugeordnet werden können. Ein Projekt kann auch
:ref:`Dokumente <dokumente>` enthalten, denen Maßnahmen zugeordnet werden
können.

Um ein Projekt anzulegen, müssen Sie zunächst die Übersicht aller Projekte
aufrufen. Klicken Sie dafür in der :ref:`navigation` auf den Button
:guilabel:`Projects`. Es öffnet sich eine Tabelle mit allen Projekten. Wenn Sie
noch kein Projekt angelegt haben, ist diese Tabelle leer.

.. _create_project:

Projekte anlegen
################

Klicken Sie auf den Button :guilabel:`Create Project` über der Tabelle aller
Projekte. Nun öffnet sich ein Dialog, in dem Sie die Daten für das neue Projekt
eingeben können:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Name`
     - Vergeben Sie einen aussagekräftigen Namen für Ihr Projekt.
     - Ja
   * - :guilabel:`Description`
     - Hier können Sie Ihr Projekt mit einem kurzen Text beschreiben.
     - 
   * - :guilabel:`JIRA Project`
     - Hier können Sie ein JIRA-Projekt auswählen, das mit Ihrem Projekt
       verknüpft werden soll. Tickets, die das MV-Tool für Maßnahmen dieses
       Projekts anlegt, werden dann in diesem JIRA-Projekt angelegt.
     - 

Bestätigen Sie Ihre Eingaben mit dem Button :guilabel:`Save`. Anschließend wird
neu angelegte Projekt in der Liste der Projekte angezeigt.

.. note::

    Sie können die Daten Ihres Projekts jederzeit bearbeiten. Nutzen Sie dafür
    die :ref:`Eintrag-spezifischen Funktionen <eintrag-spezifische-funktionen>`
    des MV-Tools.

Projekt öffnen
##############

Um an einem Projekt zu arbeiten, müssen Sie es zunächst öffnen. Klicken Sie
dafür einfacht auf den Eintrag des Projekts in der Tabelle aller Projekte.

.. _anforderungen:

Anforderungen
#############

Um die Anforderungen eines Projekts anzuzeigen, klicken Sie in der Tabelle der
Projekte auf den Eintrag des Projekts, dessen Anforderungen Sie anzeigen
möchten. Stellen Sie anschließend sicher, dass als letzter Eintrag der
:ref:`breadcrumbs` der Eintrag :guilabel:`Requirements` ausgewählt ist. Es wird
eine Tabelle mit allen Anforderungen des Projekts angezeigt.

Anforderung anlegen
===================

Klicken Sie auf den Button :guilabel:`Create Requirement` über der Tabelle aller
Anforderungen. Nun öffnet sich ein Dialog, in dem Sie die Daten für die neue
Anforderung eingeben können:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Reference`
     - Vergeben Sie eine eindeutige Referenz für Ihre Anforderung.
   * - :guilabel:`Summary`
     - Schreiben sie eine aussagekräftige Kurzzusammenfassung für Ihre
       Anforderung. Diese kann ein Satz sein oder auch nur ein paar Stichworte.
     - Ja
   * - :guilabel:`Description`
     - Hier können Sie den Inhalt Ihrer Anforderung ausführlich beschreiben, sofern 
       dieser aus der Zusammenfassung nicht eindeutig hervorgeht.
     - 
   * - :guilabel:`Milestone`
     - Hier könnnen Sie einen Meilenstein definieren zu dem Sie die Anforderung
       umgesetzt haben möchten.
     - 
   * - :guilabel:`Target object`
     - Hier können Sie ein Zielobjekt auswählen, auf das sich die Anforderung
       bezieht. I.d.R. ist dies eine bestimmte IT-Infrastruktur oder eine Gruppe
       von IT-Infrastrukturen.
     - 

Bestätigen Sie Ihre Eingaben mit dem Button :guilabel:`Save`. Anschließend wird
die neu angelegte Anforderung in der Liste der Anforderungen angezeigt.

.. note::

    Sie können die Daten Ihrer Anforderung jederzeit bearbeiten. Nutzen Sie
    dafür die :ref:`Eintrag-spezifischen Funktionen
    <eintrag-spezifische-funktionen>` des MV-Tools. Außerdem können Sie den
    :ref:`Erfüllungsgrad <compliance>` Ihrer Anforderung definieren.


.. _dokumente:

Dokumente
#########

.. _massnahmen:

Maßnahmen
#########