<p align="center">
  <a href="https://efacamverse.lebert.ai/"><img src="assets/og_camverse.png" alt="EFA CAMverse – 9 PCB/CAM-Formate. Eine Ansicht." width="100%"></a>
</p>

<p align="center">
  <a href="README.md">English</a> &nbsp;·&nbsp; <b>Deutsch</b>
</p>

<p align="center">
  <a href="https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/latest"><img alt="Aktuelles Release" src="https://img.shields.io/github/v/release/LEBERT-Software-Engineering/EFA-CAMverse?label=aktuelles%20Release&color=1e5aa8"></a>
  <a href="https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/LEBERT-Software-Engineering/EFA-CAMverse/total?label=Downloads&color=0bb4cf"></a>
  <img alt="Windows 10 / 11, 64-bit" src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-555">
  <a href="https://efacamverse.lebert.ai/"><img alt="Website" src="https://img.shields.io/badge/Website-efacamverse.lebert.ai-1e5aa8"></a>
</p>

# <img src="assets/icon_camverse.png" width="36" alt="" valign="middle"> EFA CAMverse

**9 PCB/CAM-Formate. Eine Ansicht.** EFA CAMverse öffnet Gerber X3, EAGLE, ODB++, IPC-2581, GenCAD, IPC-D-356, DXF, PADS und KiCad in einem einzigen nativen Windows-Tool – Lagen, Stackup, Bohrungen, Bauteile und Netzlisten auf einen Blick, in 2D und 3D.

<p align="center"><b>9</b> Formate nativ &nbsp;·&nbsp; <b>1</b> Werkzeug, On-Premise &nbsp;·&nbsp; <b>100 %</b> lokal &amp; sicher</p>

> **Neu:** Aus Gerber X/X2 + Koordinaten wird Gerber X3 (für die Bestückung) → [mehr dazu](#gerber-x3)

<br>

<h2 align="center">Download</h2>

<p align="center">
  <a href="https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/latest"><img alt="EFA CAMverse 2026 herunterladen" src="https://img.shields.io/badge/Download-EFA%20CAMverse%202026%20f%C3%BCr%20Windows-1e5aa8?style=for-the-badge"></a>
  &nbsp;
  <a href="https://efacamverse.lebert.ai/"><img alt="Produkt-Website" src="https://img.shields.io/badge/Website-efacamverse.lebert.ai-555?style=for-the-badge"></a>
</p>

| Datei | Zweck |
|---|---|
| [`EFA_CAMverse_2026_Setup_x64.exe`](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/latest/download/EFA_CAMverse_2026_Setup_x64.exe) | **Empfohlen.** Setup-Paket inklusive Visual-C++-Laufzeit; interaktive Installation, eine vorhandene Installation wird an Ort und Stelle aktualisiert. |
| [`EFA_CAMverse_2026_x64.msi`](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/latest/download/EFA_CAMverse_2026_x64.msi) | Reines Windows-Installer-Paket für Administratoren und Softwareverteilung (benötigt das Visual C++ 2015–2022 x64 Redistributable). |
| `SHA256SUMS.txt` | SHA-256-Prüfsummen der obigen Dateien, liegt jedem Release bei. |

Windows 10 oder 11, 64-bit. EFA CAMverse ist als Viewer kostenlos nutzbar – höherwertige Funktionen schalten Sie bei Bedarf frei. Nativ unter Windows, Ihre Daten bleiben lokal. Die Anwendung weist gelegentlich auf weitere Produkte der EFA SmartSuite hin und prüft beim Start auf Updates.

<details>
<summary><b>Windows SmartScreen beim ersten Start</b></summary>
<br>
Da EFA CAMverse gerade erst veröffentlicht wurde, zeigt Windows beim ersten Start noch einen SmartScreen-Sicherheitshinweis („Der Computer wurde durch Windows geschützt“). Das ist normal – die App ist mit einem EV-Zertifikat signiert und sicher. So lässt sie sich starten: <b>Weitere Informationen</b> → <b>Trotzdem ausführen</b>.
</details>

<details>
<summary><b>Signatur und Prüfsumme prüfen</b></summary>
<br>
Alle Binärdateien sind mit einem Extended-Validation-Code-Signing-Zertifikat signiert, ausgestellt auf <b>LEBERT Software Engineering GmbH &amp; Co. KG</b>. In PowerShell:

```powershell
Get-AuthenticodeSignature .\EFA_CAMverse_2026_Setup_x64.exe | Format-List Status, SignerCertificate
Get-FileHash .\EFA_CAMverse_2026_Setup_x64.exe -Algorithm SHA256
```

Den Hash mit der `SHA256SUMS.txt` des Releases vergleichen.
</details>

<br>

<h2 align="center">Unterstützte Formate</h2>

<p align="center"><b>Ein Viewer für alle PCB/CAM-Formate.</b> EFA CAMverse liest jedes Format nativ – von der Konstruktion bis zur Fertigungsprüfung, ohne Konvertierung und ohne Cloud.</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/formats_strip_dark.png">
    <img src="assets/formats_strip_light.png" width="100%" alt="Unterstützte Formate: Gerber X/X2/X3, EAGLE, ODB++, IPC-2581, GenCAD 1.4, IPC-D-356, DXF, PADS Layout, KiCad">
  </picture>
</p>

<details>
<summary><b>Dateitypen und Details</b></summary>
<br>

| Format | | |
|---|---|---|
| **Gerber X/X2/X3** | `.gbr` `.ger` `.gtl` `.gbl` … `.pho` · `.drl` · `.gbrjob` | RS-274X & Excellon-Bohrdaten, inkl. Gerber-Jobdatei |
| **EAGLE** | `.brd` | Board-Dateien nativ öffnen – ohne Import |
| **ODB++** | `.tgz` `.tar.gz` `.zip` | Lagen, Netze & Stackup ansehen |
| **IPC-2581** | `.xml` `.cvg` `.zip` | Offener Industriestandard (DPMX) |
| **GenCAD 1.4** | `.cad` `.gcd` `.pnl` | Bestückdaten – Import & Export · *einzigartig* |
| **IPC-D-356** | `.ipc` `.356` `.d356` | Bare-Board-Netzliste & Testdaten · *einzigartig* |
| **DXF** | `.dxf` | Mechanik & Bestückung (AutoCAD) |
| **PADS Layout** | `.asc` | Nativ ansehen (Siemens/Mentor) · *einzigartig* |
| **KiCad** | `.kicad_pcb` `.kicad_pro` | Board- und Projektdateien öffnen |

</details>

<br>

<a id="gerber-x3"></a>
<p align="center"><sub><b>NEU · FÜR EMS-DIENSTLEISTER</b></sub></p>
<h2 align="center">Gerber X/X2 + Koordinaten = Gerber X3 (Bestückung)</h2>

**Der EMS-Alltag:** Der Kunde liefert klassische Gerber-Daten ohne Bauteilinformation – und irgendeine Pick-&-Place-Datei. EFA CAMverse führt beides zusammen und ergänzt die komplette Bauteilebene, wie man sie sonst nur von Gerber X3 kennt.

<p align="center">
  <img src="assets/x3_equation.png" width="100%" alt="Gerber-X/X2-Lagen (.gbr) plus Koordinatendatei (.csv/.txt) ergeben eine bestückte Leiterkarte – Gerber X3 (für die Bestückung)">
</p>

- **Koordinatendatei laden – fertig:** EFA CAMverse ordnet jedem Bauteil automatisch Pads, Bestückungsdruck-Umriss und Bohrungen zu.
- **Kein Umformatieren nötig:** Spaltenaufbau, Trenn- und Dezimalzeichen, Maßeinheit und Seitenangabe erkennt EFA CAMverse selbst – auch ohne Kopfzeile. Sie laden die Liste, wie Ihr Kunde sie liefert, ob aus Altium, KiCad, EAGLE, …
- **Nachvollziehbar statt Blackbox:** Ein Bericht zeigt nach jedem Lauf, welche Bauteile sicher zugeordnet sind und welche nicht. Sitzt eines falsch, setzen Sie es mit zwei Klicks im Bild an die richtige Stelle.
- **Ab jetzt wie echtes X3:** Bestückungsansichten, Varianten, Stückliste und 3D stehen zur Verfügung, als hätte der Datensatz seine Bauteile immer gekannt. Die geprüften Koordinaten geben Sie als CSV aus – für die Maschinenprogrammierung oder zurück an den Kunden.

<br>

<h2 align="center">Funktionen</h2>

<p align="center"><b>Sehen. Prüfen. Fertigen.</b> Ein einheitlicher Funktionssatz über alle Formate – statt für jedes Format ein anderes Werkzeug.</p>

<table>
  <tr>
    <td align="center" valign="top" width="33%"><br><img src="assets/feat_layers.png" width="48" alt=""><br><br><b>Lagen &amp; Stackup</b><br>Alle Lagen einzeln schalten, Transparenz regeln und den kompletten Materialaufbau im Stackup-Pane lesen.<br><br></td>
    <td align="center" valign="top" width="33%"><br><img src="assets/feat_3d.png" width="48" alt=""><br><br><b>3D-Ansicht</b><br>Die Leiterkarte räumlich betrachten – mit Bauteilen als 3D-Körper, frei drehen und zoomen.<br><br></td>
    <td align="center" valign="top" width="33%"><br><img src="assets/feat_netlist.png" width="48" alt=""><br><br><b>Bohrungen &amp; Netze</b><br>Bohrtabellen, Netzlisten-Pane und bidirektionales Highlight – per Doppelklick zum Netz zoomen.<br><br></td>
  </tr>
  <tr>
    <td align="center" valign="top"><br><img src="assets/feat_components.png" width="48" alt=""><br><br><b>Bestückung &amp; Varianten</b><br>Bestückungsansichten flexibel erstellen – Bauteile passend zur Kundenvariante per Klick ein- und ausblenden, Beschriftung frei wählbar.<br><br></td>
    <td align="center" valign="top"><br><img src="assets/feat_x3.png" width="48" alt=""><br><br><b>Gerber X/X2 + Koordinaten = X3</b><br>Klassische Gerber-Daten um externe Koordinatendaten ergänzen – EFA CAMverse führt beides zu Gerber X3 (für die Bestückung) zusammen.<br><br></td>
    <td align="center" valign="top"><br><img src="assets/feat_exportfile.png" width="48" alt=""><br><br><b>Export &amp; Fertigen</b><br>Für die Fertigung exportieren: Bilder als PDF, PNG oder JPG, Koordinaten und BoM als CSV.<br><br></td>
  </tr>
  <tr>
    <td align="center" valign="top"><br><img src="assets/feat_measure.png" width="48" alt=""><br><br><b>Messen &amp; Inspizieren</b><br>Präzise Abstands- und Geometriemessung – mit Hüllrechteck und Mittelpunkt jeder Komponente.<br><br></td>
    <td align="center" valign="top"><br><img src="assets/feat_export.png" width="48" alt=""><br><br><b>Formate wandeln &amp; GenCAD</b><br>Eingelesene Daten als GenCAD 1.4 weitergeben – echte Konvertierung, nicht nur Anzeige.<br><br></td>
    <td align="center" valign="top"><br><img src="assets/feat_offline.png" width="48" alt=""><br><br><b>Offline &amp; nativ</b><br>Native Windows-Anwendung – keine Cloud, kein Upload. Ihre Fertigungsdaten bleiben lokal.<br><br></td>
  </tr>
</table>

<br>

<p align="center"><sub><b>NEU · BESTÜCKDRUCK &amp; VARIANTEN</b></sub></p>
<h2 align="center">Bestückdruck &amp; Varianten</h2>

**Bestückdruck selbst erzeugen – so, wie die Fertigung ihn braucht.** EFA CAMverse zeigt keinen gelieferten Bestückplan an, sondern zeichnet ihn aus den Daten selbst – Bauteil für Bauteil. Genau deshalb lässt sich die Variante Ihres Kunden wirklich abbilden: Was nicht bestückt wird, erscheint gar nicht erst.

<p align="center">
  <img src="assets/assembly_board.png" width="49%" alt="Bestückungsdruck – Vollbestückung">
  <img src="assets/assembly_board_variant.png" width="49%" alt="Bestückungsdruck – Kundenvariante mit ausgeblendeten Bauteilen">
</p>
<p align="center"><sub><b>Vollbestückung</b> &nbsp;⇄&nbsp; <b>Kundenvariante</b> – abgewählte Bauteile verschwinden vollständig</sub></p>

- **Variantenhandling:** Komponenten per Klick ab- und wieder anwählen – abgewählte Bauteile verschwinden vollständig, mit Gehäuse, Pads und Beschriftung. Aus der gelieferten Vollbestückung wird so die Variante des Kunden, in 2D wie in 3D.
- **Beschriftung, selektiv:** Jedes Bauteil wird automatisch mit seiner Referenz beschriftet – Testpunkte, Passermarken oder ganze Gruppen blenden Sie per Namensmuster aus. Schriftart und Schriftgröße wählen Sie frei.
- **Farben nach Ihrer Vorgabe:** Platinenfläche, Rand, Gehäuse, Pads, Pin-1-Marker und Beschriftung haben je eine eigene Farbe – Pads, Pin-1 und Beschriftung lassen sich auch ganz abschalten.
- **Lage dazublenden:** Jede beliebige Lage – etwa Lötstopp oder Bohrbild – legen Sie farbig und transparent über den Bestückdruck.
- **Beide Seiten:** Ober- und Unterseite als jeweils eigene Bestückungsansicht.
- **Ausgabe:** Bestückplan, Koordinatendaten und Stückliste für die Fertigung exportieren.

<br>

<p align="center"><sub><b>NEU · 3D-ANSICHT</b></sub></p>
<h2 align="center">3D-Ansicht</h2>

**Die Leiterkarte in 3D – interaktiv und realistisch.** Ein Klick wechselt von der Lagenansicht in die räumliche Darstellung: Leiterkarte, Oberflächen und Bauteile als echtes 3D-Modell – frei dreh- und zoombar.

<p align="center">
  <img src="assets/view3d_board.jpg" width="438" alt="EFA CAMverse 3D-Ansicht: bestückter Leiterplatten-Nutzen mit Bauteilen als 3D-Modelle">
</p>

- **Realistisch extrudierte Leiterkarte:** Substrat, Lötstopplack und Oberflächen wie am fertigen Board.
- **Bauteile als 3D-Körper:** automatisch erzeugt – auf Wunsch mit echten 3D-Modellen aus dem nachladbaren Modellpaket.
- **Modelle zuordnen:** komfortabel per Suche und 3D-Vorschau im Zuordnungs-Dialog.
- **Frei drehen und zoomen:** ausgeblendete Bauteile der Variante verschwinden live auch in 3D.

Das optionale **3D-Modellpaket** (KiCad-3D-Bibliotheksmodelle im VRML-Format, CC-BY-SA 4.0) wird als eigenes [Release](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/tag/3dmodels-9.0.0) veröffentlicht; EFA CAMverse lädt und installiert es aus der Anwendung heraus.

<br>

<h2 align="center">Warum EFA CAMverse</h2>

<p align="center"><b>9 PCB/CAM-Formate. Eine Anwendung. Ein Workflow.</b> Ein vertrautes Bedienkonzept für jedes Format: einmal einarbeiten, dann Gerber, ODB++, KiCad und sechs weitere Formate gleich bedienen.</p>

- **Ein Bedienkonzept für alles** – einmal einarbeiten, dann jedes Format identisch bedienen: Lagen, Stackup, Messen und Export funktionieren überall gleich.
- **Direkt nativ, ohne Umwege** – jedes Format ohne Zwischenkonvertierung öffnen und sofort arbeiten; kein Export-Import-Hin-und-Her zwischen Programmen.
- **Formate Seite an Seite** – verschiedene Formate desselben Projekts in einer Oberfläche öffnen und gemeinsam betrachten.
- **Brücke zwischen Formaten** – aus jedem der 9 PCB/CAM-Formate lesen und als GenCAD 1.4 weitergeben; EFA CAMverse verbindet, was sonst getrennt bleibt.
- **Eine Installation, ein Update** – eine Anwendung statt vieler Einzeltools pflegen: ein Update, ein Ansprechpartner, alles lokal.

<br>

<h2 align="center">Viewer kostenlos &amp; Pro-Funktionen</h2>

<p align="center">EFA CAMverse ist als Viewer kostenlos nutzbar – höherwertige Funktionen schalten Sie bei Bedarf frei.</p>

**Pro-Funktionen:**

1. Erstellen von **Bestückungsansichten** (Ober-/Unterseite) inkl. **konfigurierbarem Bestückungsdruck**
2. **Export**: Koordinaten & BoM als CSV, Netzliste
3. **Konvertierungen** der PCB/CAM-Formate
4. … und vieles mehr

<br>

<h2 align="center">Über dieses Repository</h2>

EFA CAMverse ist proprietäre Closed-Source-Software von LEBERT Software Engineering. Dieses Repository enthält **keinen** Quellcode – es ist die öffentliche Anlaufstelle für die **Installationsdateien** ([Releases](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases)), das **[Änderungsprotokoll](CHANGELOG.md)** sowie **Fehlermeldungen und Funktionswünsche** ([Issues](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/issues)).

**Support & Feedback**

- Fehler gefunden oder Funktion vermisst? [Issue anlegen](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/issues/new/choose) – auf Deutsch oder Englisch.
- Fragen, Lizenzierung, vertrauliche Beispieldaten: [EFA_CAMverse@lse.cc](mailto:EFA_CAMverse@lse.cc)
- Produkt-Website: [efacamverse.lebert.ai](https://efacamverse.lebert.ai/)

<br>

<h2 align="center">Rechtliches</h2>

<p align="center"><a href="https://lebert.org"><img src="assets/logo_lse.png" width="140" alt="LSE – LEBERT Software Engineering"></a></p>

EFA CAMverse ist Teil der **EFA SmartSuite** für die Elektronikfertigung – entwickelt von [LEBERT Software Engineering](https://lebert.org).
© 2026 LEBERT Software Engineering GmbH & Co. KG. Alle Rechte vorbehalten. Die Nutzung der Software unterliegt den [Lizenzbedingungen](LICENSE.md); sie enthält Open-Source-Komponenten (OpenCV, pugixml, earcut.hpp, libzip, zlib) unter ihren jeweiligen Lizenzen, das optionale 3D-Modellpaket enthält KiCad-Bibliotheksmodelle unter CC-BY-SA 4.0 – siehe [LICENSE.md](LICENSE.md). Alle Marken sind Eigentum ihrer jeweiligen Inhaber.

<p align="center"><sub><a href="https://lebert.org/impressum">Impressum</a> · <a href="https://lebert.org/datenschutzerklaerung">Datenschutz</a></sub></p>
