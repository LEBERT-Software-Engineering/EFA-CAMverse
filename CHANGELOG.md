# Changelog

All notable changes to **EFA CAMverse** are documented in this file. Each entry has an English and a German part.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versions refer to the application
version shown in *Help → About* (the product is marketed as "EFA CAMverse 2026").

Alle wesentlichen Änderungen an **EFA CAMverse** werden hier festgehalten – je Eintrag auf Englisch und Deutsch.

## [Unreleased]

## [3.6.2] - 2026-09-16

### English

- **Assembly view – labels the way you want them:** move any reference label by hand, rotate it, undo and redo
  your changes, and reset everything to automatic placement with one click. Instead of the reference designator
  the label can show any component field – value, package, part number and more – for all components or by rule
  per component type. A smaller minimum font size suits dense boards.
- **Large data without waiting in the dark:** a progress dialog shows the loading state for all nine formats, and
  the rendering resolution adapts to the board size and the available memory – no more frozen windows, no more
  aborts on machines with less memory.
- **Multi-up panels in the assembly view:** ODB++ panels are shown with every single board, including component
  hover and *Hide text* across the whole panel.
- **Silkscreen text removal works on Altium data:** *Hide text* in the layer view, the assembly overlay and the
  GenCAD export option now also remove the labels of Altium exports, keeping the component outlines.
- **IPC-2581:** components are placed on the correct side, line widths are rendered as designed, and large files
  load faster.
- **Altium ODB++:** umlauts and special characters in component data are shown correctly.
- **Fixed:** *Reload* (Ctrl+R) for GenCAD, EAGLE, KiCad, IPC-2581 and ODB++; cancelling the save prompt on exit
  left the application unresponsive; unsaved project changes are now confirmed before closing.

### Deutsch

- **Bestückungsansicht – Beschriftungen so, wie Sie sie wollen:** jede Referenzbeschriftung von Hand verschieben,
  drehen, Änderungen rückgängig machen und wiederholen, alles mit einem Klick auf Automatik zurücksetzen. Statt
  der Referenz zeigt die Beschriftung auf Wunsch jedes Bauteilfeld – Wert, Gehäuse, Artikelnummer und mehr – für
  alle Bauteile oder per Regel je Bauteiltyp. Eine kleinere Mindestschriftgröße passt zu dichten Platinen.
- **Große Daten ohne Warten im Dunkeln:** ein Fortschrittsdialog zeigt den Ladestand für alle neun Formate, und
  die Darstellungsauflösung richtet sich nach Platinengröße und verfügbarem Arbeitsspeicher – kein eingefrorenes
  Fenster mehr, keine Abbrüche auf Rechnern mit weniger Speicher.
- **Mehrfachnutzen in der Bestückungsansicht:** ODB++-Nutzen erscheinen mit allen Einzelschaltungen, inklusive
  Bauteil-Hover und „Schriftzüge ausblenden" über den ganzen Nutzen.
- **Schriftzüge entfernen auch bei Altium-Daten:** „Schriftzüge ausblenden" in der Lagenansicht, das Bestückungs-
  Overlay und die GenCAD-Exportoption entfernen jetzt auch die Beschriftung von Altium-Exporten; die Bauteilumrisse
  bleiben erhalten.
- **IPC-2581:** Bauteile liegen auf der richtigen Seite, Linienbreiten erscheinen wie entworfen, große Dateien
  laden schneller.
- **Altium-ODB++:** Umlaute und Sonderzeichen in Bauteildaten werden korrekt angezeigt.
- **Behoben:** „Neu laden" (Strg+R) bei GenCAD, EAGLE, KiCad, IPC-2581 und ODB++; nach „Abbrechen" in der
  Sicherungs-Rückfrage beim Beenden reagierte das Programm nicht mehr; ungesicherte Projektänderungen werden jetzt
  vor dem Schließen abgefragt.

## [3.5.4] - 2026-09-01

### English

Covers everything since 3.2.1 (versions 3.3.x and 3.4.x were not released on GitHub).

- **Projects – your whole working state in one file:** layers, colours, visibility, the assembly variant, the assigned
  coordinate data and your assembly-drawing settings are stored in a project file. Reopen a job weeks later exactly as
  you left it, on any workstation; the source data can travel inside the project, so you pass on a single file.
  Works for all nine supported CAM formats, not just Gerber.
- **Closer integration with EFA SmartSuite:** start EFA CAMverse straight from SmartSuite, prepare the data and hand
  the finished state back to the project – no clipboard, no hunting through the file system.
- **Excel export:** coordinate lists, bills of material and netlists can now be written directly as an Excel workbook
  in addition to CSV. For the BoM you choose how items are grouped.
- **GenCAD 1.4 export extended:** more faithful board data for the round trip into EFA SmartSuite; the option to drop
  all text from the silkscreen layers is now available for Gerber sources as well.
- **Board outline detection fixed:** Altium mechanical layers such as `.GM13`/`.GM15` were mistaken for the board
  profile because the file-extension test matched too loosely. Sets without a recognisable profile layer now derive
  the board area from the copper, so the assembly drawing always shows a proper board surface.
- **Assembly drawing:** the layer shown as an overlay now follows the side – switching to the bottom side no longer
  leaves the top silkscreen on screen.
- Several CAM formats open and render noticeably faster; many detail improvements and fixes.

### Deutsch

Umfasst alle Änderungen seit 3.2.1 (die Versionen 3.3.x und 3.4.x wurden nicht auf GitHub veröffentlicht).

- **Projekte – der komplette Arbeitsstand in einer Datei:** Lagen, Farben, Sichtbarkeiten, die Bestückungsvariante,
  die zugeordneten Koordinatendaten und die Einstellungen für den Bestückdruck wandern in eine Projektdatei. Ein
  Auftrag lässt sich Wochen später genau so wieder öffnen, wie er verlassen wurde – auch am nächsten Arbeitsplatz;
  die Quelldaten können im Projekt mitreisen, sodass nur EINE Datei weitergegeben wird. Gilt für alle neun
  unterstützten CAM-Formate, nicht nur für Gerber.
- **Engere Verzahnung mit EFA SmartSuite:** EFA CAMverse startet direkt aus der SmartSuite heraus; der aufbereitete
  Stand geht anschließend an das Projekt zurück – ohne Zwischenablage, ohne Suchen im Dateisystem.
- **Excel-Export:** Koordinatenlisten, Stücklisten und Netzlisten lassen sich jetzt neben CSV auch direkt als
  Excel-Arbeitsmappe ausgeben. Bei der Stückliste ist die Art der Zusammenfassung wählbar.
- **GenCAD-1.4-Export ausgebaut:** verlässlichere Boarddaten für den Rückweg in die EFA SmartSuite; die Option, alle
  Textelemente von den Silk-Lagen zu entfernen, steht nun auch für Gerber-Quellen zur Verfügung.
- **Konturerkennung korrigiert:** Altium-Mechaniklagen wie `.GM13`/`.GM15` galten als Platinenkontur, weil der
  Endungsvergleich zu unscharf war. Datensätze ohne erkennbare Konturlage leiten die Platinenfläche jetzt aus dem
  Kupfer ab – der Bestückdruck zeigt damit immer eine saubere LP-Oberfläche.
- **Bestückdruck:** die eingeblendete Lage folgt der Seite – beim Wechsel auf die Unterseite bleibt nicht länger der
  Bestückungsdruck der Oberseite stehen.
- Diverse CAM-Formate öffnen und zeichnen spürbar zügiger; dazu viele Detailverbesserungen und Fehlerbehebungen.

## [3.2.1] - 2026-08-23

### English

First release published on GitHub. Highlights of the current feature set:

- **Gerber X/X2 + coordinates = Gerber X3 (for assembly):** load a pick & place file (CSV/TXT, column layout,
  separators, units and board side are detected automatically) and EFA CAMverse assigns pads, silkscreen outline
  and drill holes to every component – with an assignment report and two-click correction in the image. The verified
  coordinates can be exported as CSV.
- **Assembly drawing & variants:** the assembly drawing is generated from the data, component by component;
  components can be deselected for a customer variant and disappear completely (body, pads, labelling) – in 2D and 3D.
  Selective labelling by name pattern, free choice of font, individual colours, any layer as a semi-transparent overlay,
  top and bottom as separate views.
- **3D view:** realistically extruded board with solder mask and surfaces, components as automatically generated
  3D bodies – optionally with real KiCad models from the downloadable 3D model pack; model assignment dialog with
  search and 3D preview.
- Nine formats natively: Gerber X/X2/X3 (RS-274X, Excellon, .gbrjob), EAGLE, ODB++, IPC-2581, GenCAD 1.4 (import
  & export), IPC-D-356, DXF, PADS Layout (.asc), KiCad.

Earlier versions were not tracked on GitHub.

### Deutsch

Erste auf GitHub veröffentlichte Version. Highlights des aktuellen Funktionsumfangs:

- **Gerber X/X2 + Koordinaten = Gerber X3 (für die Bestückung):** Pick-&-Place-Datei laden (CSV/TXT; Spaltenaufbau,
  Trennzeichen, Einheit und Seite werden automatisch erkannt) – EFA CAMverse ordnet jedem Bauteil Pads,
  Bestückungsdruck-Umriss und Bohrungen zu, mit Zuordnungsbericht und Zwei-Klick-Korrektur im Bild. Die geprüften
  Koordinaten lassen sich als CSV ausgeben.
- **Bestückdruck & Varianten:** Der Bestückdruck wird Bauteil für Bauteil aus den Daten erzeugt; Bauteile lassen sich
  für eine Kundenvariante abwählen und verschwinden vollständig (Gehäuse, Pads, Beschriftung) – in 2D und 3D.
  Selektive Beschriftung per Namensmuster, freie Schriftwahl, eigene Farben, beliebige Lage als transparente
  Überlagerung, Ober- und Unterseite als eigene Ansichten.
- **3D-Ansicht:** realistisch extrudierte Leiterkarte mit Lötstopplack und Oberflächen, Bauteile als automatisch
  erzeugte 3D-Körper – auf Wunsch mit echten KiCad-Modellen aus dem nachladbaren 3D-Modellpaket;
  Zuordnungs-Dialog mit Suche und 3D-Vorschau.
- Neun Formate nativ: Gerber X/X2/X3 (RS-274X, Excellon, .gbrjob), EAGLE, ODB++, IPC-2581, GenCAD 1.4 (Import
  & Export), IPC-D-356, DXF, PADS Layout (.asc), KiCad.

Ältere Versionen wurden nicht auf GitHub geführt.

[Unreleased]: https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/compare/v3.5.4...HEAD
[3.5.4]: https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/compare/v3.2.1...v3.5.4
[3.2.1]: https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/tag/v3.2.1
