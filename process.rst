.. _prozess:

###################
Maßnahmenverfolgung
###################

Der Prozess der Maßnahmenverfolgung ermöglicht es Ihnen, den Fortschritt Ihrer
Projektanforderungen und Maßnahmen zu überwachen und zu verwalten. Dieser
Abschnitt führt Sie durch die wesentlichen Komponenten dieses Prozesses:
Erfüllungsgrad, Änderung des Erfüllungsgrades, JIRA-Tickets, Umsetzung,
Überprüfung und Änderung des Umsetzungsstands.

.. _compliance:

Erfüllungsgrad
##############

Der Erfüllungsgrad dient der Nachverfolgung der Einhaltung einer
:ref:`Anforderung <anforderungen>` oder :ref:`Maßnahme <massnahmen>` in Ihrem
Projekt. Er findet Anwendung in unterschiedlichen Kontexten, wie z.B.
vertraglichen Vereinbarungen mit Ihren Kunden oder der Einhaltung gesetzlicher
Vorschriften.

Der Erfüllungsgrad wird durch die folgenden Statusangaben bestimmt:

.. list-table::
   :header-rows: 1

   * - Status
     - Beschreibung
   * - :guilabel:`Compliant`, :guilabel:`C`
     - Zeigt an, dass die Anforderung oder Maßnahme vollständig erfüllt wird.
   * - :guilabel:`Partially compliant`, :guilabel:`PC`
     - Bedeutet, dass die Anforderung oder Maßnahme nur teilweise erfüllt ist.
       Es gibt jedoch noch Aspekte, die besondere Beachtung erfordern, weil sie
       aus verschiedenen Gründen nicht vollständig erfüllt werden können.
   * - :guilabel:`Not applicable`, :guilabel:`N/A`
     - Zeigt an, dass die Anforderung oder Maßnahme nicht auf Ihr Projekt
       anwendbar ist und daher nicht berücksichtigt werden muss.
   * - :guilabel:`Not compliant`, :guilabel:`NC`
     - Signalisiert, dass die Anforderung oder Maßnahme derzeit nicht erfüllt
       wird und ggf. Handlungsbedarf besteht, um sie dennoch erfüllen zu können.

.. _edit_compliance:

Änderung des Erfüllungsgrades
=============================

Um den Erfüllungsgrad einer :ref:`Anforderung <anforderungen>` oder
:ref:`Maßnahme <massnahmen>` zu ändern, wählen Sie die Option 
:guilabel:`Set compliance` im Menü der :ref:`eintrag-spezifischen
Funktionen<eintrag-spezifische-funktionen>` der jeweiligen Anforderung oder
Maßnahme.

Der Dialog zur Änderung des Erfüllungsgrades enthält die folgenden Felder:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Compliance status`
     - Hier legen Sie den neuen :ref:`Erfüllungsgrad <compliance>` der
       Anforderung oder Maßnahme fest.
     - 
   * - :guilabel:`Compliance comment`
     - In diesem Feld können Sie zusätzliche Informationen oder Begründungen für
       die Festlegung des Erfüllungsgrades angeben. Der Kommentar ist nur
       verfügbar, wenn ein Erfüllungsgrad ausgewählt wurde.
     - 

Klicken Sie auf :guilabel:`Save`, um Ihre Eingaben zu bestätigen und den
Erfüllungsgrad der Anforderung oder Maßnahme entsprechend zu aktualisieren.

Der Erfüllungsgrad kann auch direkt in der Tabellenansicht geändert werden.
Klicken Sie hierfür auf den entsprechenden Wert in der Spalte
:guilabel:`Compliance`, sofern diese sichtbar ist. Die Spalte
:guilabel:`Compliance` wird automatisch angezeigt, sobald für mindestens eine
Anforderung oder Maßnahme in Ihrem Projekt ein Erfüllungsgrad festgelegt wurde.

.. hint::

    Beachten Sie, dass Anforderungen oder Maßnahmen, bei denen der Erfüllungsgrad
    als :guilabel:`Not applicable` oder :guilabel:`Not compliant` festgelegt
    wurde, bei der Berechnung des Umsetzungsstands durch das MV-Tool
    nicht berücksichtigt werden.

.. _jira_issues:

JIRA-Tickets
############

Es ist möglich, ein JIRA-Ticket mit einer :ref:`Maßnahme <massnahmen>` zu
verknüpfen. Das ist vor allem dann hilfreich, wenn die Maßnahme technisch
komplex ist und daher in JIRA nachverfolgt werden sollte.

Die Verknüpfung eines JIRA-Tickets mit einer Maßnahme kann direkt in der
:ref:`Tabellenansicht <massnahmen>` durchgeführt werden. Klicken Sie hierzu auf
den Button :guilabel:`Add issue` in der Spalte :guilabel:`JIRA issue` der
entsprechenden Maßnahme. Danach öffnet sich ein Dropdown-Menü, in dem Sie
entweder ein neues JIRA-Ticket erstellen (:guilabel:`Create issue`) oder ein
bereits vorhandenes JIRA-Ticket auswählen können (:guilabel:`Select issue`).

JIRA-Ticket erstellen
=====================

Wenn Sie ein neues JIRA-Ticket erstellen möchten, wählen Sie die Option
:guilabel:`Create issue` aus dem :ref:`Dropdown-Menü <jira_issues>` aus.
Daraufhin öffnet sich ein Dialogfenster mit
folgenden Eingabefeldern:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Issue type`
     - In diesem Feld werden die verfügbaren JIRA-Ticket-Typen des JIRA-Projekts
       angezeigt, das Sie mit Ihrem Projekt verknüpft haben. Wählen Sie den
       gewünschten Ticket-Typ aus.
     - Ja
   * - :guilabel:`Summary`
     - Geben Sie hier eine kurze Zusammenfassung des JIRA-Tickets an.
       Diese wird in JIRA als Titel des Tickets verwendet. Dieses Feld ist
       bereits mit der Zusammenfassung Ihrer :ref:`Maßnahme <maßnahmen>`
       vorausgefüllt, kann aber angepasst werden.
     - Ja
     - :guilabel:`Description`
     - Geben Sie hier eine ausführliche Beschreibung des JIRA-Tickets
       an. Diese wird in JIRA als Beschreibung des Tickets verwendet.
       Dieses Feld ist bereits mit der Beschreibung Ihrer :ref:`Maßnahme
       <maßnahmen>` vorausgefüllt, kann aber nach Belieben angepasst werden.
     -

Bestätigen Sie Ihre Eingaben mit dem Button :guilabel:`Create`. Anschließend
wird das JIRA-Ticket erstellt und mit der Maßnahme verknüpft. Es wird in der
Spalte :guilabel:`JIRA issue` in der :ref:`Tabellenansicht <massnahmen>`
angezeigt.

.. hint::

    Beachten Sie, dass Sie nur JIRA-Tickets erstellen können, wenn Sie Ihr
    Projekt mit einem :ref:`JIRA-Projekt verknüpft <create_project>` haben.

JIRA-Ticket auswählen
=====================

Um ein bereits existierendes JIRA-Ticket mit einer Maßnahme zu verknüpfen,
wählen Sie die Option :guilabel:`Select issue` aus dem 
:ref:`Dropdown-Menü <jira_issues>`. Danach öffnet sich ein Dialog mit einem
Suchfeld, in das Sie den Titel oder die ID des JIRA-Tickets eingeben können.
Sobald Sie mit der Eingabe beginnen, werden Ihnen passende JIRA-Tickets
angezeigt. Wählen Sie das relevante JIRA-Ticket aus und bestätigen Sie Ihre
Auswahl mit dem Button :guilabel:`Save`. Daraufhin wird das JIRA-Ticket mit der
Maßnahme verknüpft und in der Spalte :guilabel:`JIRA issue` in der
:ref:`Tabellenansicht <massnahmen>` dargestellt.

.. _umsetzung:

Umsetzung
#########

Der Umsetzungsstand dient als wichtiges Werkzeug zur Nachverfolgung des
Projektfortschritts. Er wird für jede :ref:`Maßnahme <massnahmen>` individuell
festgelegt. Normalerweise aktualisieren die Personen oder Rollen, die für die
Umsetzung verantwortlich sind, den Umsetzungsstand.

Die verschiedenen Stufen des Umsetzungsstand lauten wie folgt:

.. list-table::
   :header-rows: 1

   * - Status
     - Beschreibung
   * - :guilabel:`Open`
     - Zeigt an, dass die Umsetzung der Maßnahme noch nicht begonnen hat.
   * - :guilabel:`In progress`
     - Zeigt an, dass die Maßnahme derzeit in Bearbeitung ist, d.h., die
       verantwortliche Person oder Rolle ist dabei, sie umzusetzen.
   * - :guilabel:`Completed`
     - Dieser Status zeigt an, dass die Maßnahme vollständig umgesetzt wurde.

.. _edit_completion:

Änderung des Umsetzungsstands
=============================

Es ist einfach, den Umsetzungsstand einer :ref:`Maßnahme <massnahmen>` zu
ändern. Verwenden Sie dazu die Option :guilabel:`Set completion` im Menü der
:ref:`spezifischen Funktionen eines Eintrags<eintrag-spezifische-funktionen>`
der jeweiligen Maßnahme.

Im Dialog zur Änderung des Umsetzungstands stehen Ihnen die folgenden Felder
zur Verfügung:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Completion status`
     - In diesem Feld legen Sie den neuen :ref:`Stand der Umsetzung
       <umsetzung>` für die Maßnahme fest.
     - Ja
   * - :guilabel:`Completion comment`
     - Hier können Sie zusätzliche Informationen oder Begründungen für die
       Änderung des Umsetzungsstand angeben. Das Kommentarfeld ist nur aktiv,
       wenn zuvor ein Umsetzungsstand ausgewählt wurde.
     - Nein

Bestätigen Sie Ihre Eingaben mit dem Button :guilabel:`Save`. Der
Umsetzungsstatus der Maßnahme wird dann entsprechend aktualisiert.

Es besteht auch die Möglichkeit, den Umsetzungsstatus direkt in der
Tabellenansicht zu ändern. Klicken Sie dazu einfach auf den entsprechenden Wert
in der Spalte :guilabel:`Completion`.

.. _verification:

Überprüfungsprozess
###################

Der Überprüfungsprozess ist ein wesentliches Instrument zur Kontrolle und
Verbesserung der Qualität Ihrer Maßnahmenumsetzung. Gewöhnlich führen die
Personen oder Rollen, die für die Überprüfung verantwortlich sind, diese durch.
Diese könnten z.B. der Mitarbeiter für Informationssicherheit, der Projektleiter
oder ein externer Auditor sein.

Der Überprüfungsprozess umfasst zwei Schritte:

1. Festlegen einer :ref:`Überprüfungsmethode <verification_method>` für die
   Maßnahmen, deren Umsetzung Sie überprüfen möchten.
2. Nach der Durchführung der Überprüfung legen Sie den :ref:`Überprüfungsstatus
   <verification_status>` fest und geben ggf. einen Kommentar ab.

.. _verification_method:

Überprüfungsmethode
===================

Da das MV-Tool seinen Ursprung in der Raumfahrtindustrie hat, sind die
Überprüfungsmethoden an den 
`Standard ECSS-M-ST-40C <https://ecss.nl/standard/ecss-m-st-40c-rev-1-configuration-and-information-management/>`_
angelehnt. Das MV-Tool bietet daher die folgenden Überprüfungsmethoden zur
Auswahl an:

.. list-table::
   :header-rows: 1

   * - Überprüfungsmethode
     - Beschreibung
   * - :guilabel:`Inspection`, :guilabel:`I`
     - Diese Methode wird genutzt, wenn die Maßnahme durch Inspektion überprüft
       wird. Das bedeutet, dass die Vollständigkeit und Korrektheit der Maßnahme
       visuell kontrolliert wird.
   * - :guilabel:`Test`, :guilabel:`T`
     - Diese Methode wird angewandt, wenn die Maßnahme durch einen Test
       überprüft wird. Dabei wird die Maßnahme durch ein Skript o.ä. auf
       Vollständigkeit und Korrektheit getestet.
   * - :guilabel:`Review`, :guilabel:`R`
     - Diese Methode wird eingesetzt, wenn die Maßnahme durch Überprüfung der
       Umsetzungsdokumentation überprüft wird. Die Maßnahme wird dabei durch
       Durchsicht der Dokumentation auf Vollständigkeit und Korrektheit
       überprüft.

.. hint::

    Nur Maßnahmen, bei denen eine Überprüfungsmethode festgelegt wurde, werden
    in der Berechnung des Überprüfungsstatus durch das MV-Tool berücksichtigt.

.. _verification_status:

Überprüfungsstatus
==================

Der Überprüfungsstatus wird durch die folgenden Statusangaben bestimmt:

.. list-table::
   :header-rows: 1

   * - Status
     - Beschreibung
   * - :guilabel:`Verified`
     - Diese Option zeigt an, dass die Maßnahme vollständig überprüft wurde.
   * - :guilabel:`Partially verified`
     - Diese Option zeigt an, dass die Maßnahme nur teilweise überprüft wurde.
       Es existieren noch Bereiche, die einer weiteren Überprüfung bedürfen, da
       sie aus verschiedenen Gründen nicht vollständig geprüft werden konnten.
   * - :guilabel:`Not verified`
     - Diese Option zeigt an, dass die Maßnahme nicht überprüft werden konnte,
       was bedeutet, dass eventuell Maßnahmen ergriffen werden müssen, um sie
       überprüfen zu können.

.. _edit_verification:

Festlegen der Überprüfungsmethode und des Überprüfungsstatus
============================================================

Um die Überprüfungsmethode und des Überprüfungsstatus für eine :ref:`Maßnahme
<massnahmen>` festzulegen, verwenden Sie die Option :guilabel:`Set verification`
im Menü der :ref:`eintragsspezifischen Funktionen<eintrag-spezifische-funktionen>` 
der betreffenden Maßnahme. Im sich dann öffnenden Überprüfungsdialog finden Sie
folgende Felder:

.. list-table::
   :header-rows: 1

   * - 
     - Beschreibung
     - Erforderlich
   * - :guilabel:`Verification method`
     - Hier legen Sie die neue :ref:`Überprüfungsmethode <verification_method>`
       für die Maßnahme fest.
     - 
   * - :guilabel:`Verification status`
     - Hier legen Sie den neuen :ref:`Überprüfungsstatus <verification_status>`
       für die Maßnahme fest. Ein Überprüfungsstatus kann nur festgelegt werden,
       wenn vorher eine Überprüfungsmethode definiert wurde.
     - 
   * - :guilabel:`Verification comment`
     - In diesem Feld können Sie zusätzliche Informationen oder Begründungen für
       die Festlegung des Überprüfungsstatus angeben. Die Angabe eines
       Kommentars ist nur möglich, wenn zuvor eine Überprüfungsmethode
       festgelegt wurde.
     - 

Bestätigen Sie Ihre Eingaben mit dem Button :guilabel:`Save`. Anschließend
werden die Überprüfungsmethode und der Überprüfungsstatus der Maßnahme
entsprechend aktualisiert.

Sie können auch die Überprüfungsmethode und den Überprüfungsstatus direkt in der
:ref:`Tabellenansicht <massnahmen>` ändern. Klicken Sie dazu auf den
entsprechenden Wert in den Spalten :guilabel:`Verification method` oder
:guilabel:`Verification status`. Diese Spalten werden automatisch angezeigt,
sobald für mindestens eine Maßnahme in Ihrem Projekt eine Überprüfungsmethode
oder ein Überprüfungsstatus festgelegt wurde.