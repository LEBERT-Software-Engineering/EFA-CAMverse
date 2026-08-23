# Changelog

All notable changes to **EFA CAMverse** are documented in this file. Each entry has an English and a German part.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versions refer to the application
version shown in *Help → About* (the product is marketed as "EFA CAMverse 2026").

Alle wesentlichen Änderungen an **EFA CAMverse** werden hier festgehalten – je Eintrag auf Englisch und Deutsch.

## [Unreleased]

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

[Unreleased]: https://github.com/__ORG__/EFA-CAMverse/compare/v3.2.1...HEAD
[3.2.1]: https://github.com/__ORG__/EFA-CAMverse/releases/tag/v3.2.1
