<p align="center">
  <a href="https://efacamverse.lebert.ai/"><img src="assets/og_camverse_en.png" alt="EFA CAMverse – 9 PCB/CAM formats. One view." width="100%"></a>
</p>

<p align="center">
  <b>English</b> &nbsp;·&nbsp; <a href="README.de.md">Deutsch</a>
</p>

<p align="center">
  <a href="https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/LEBERT-Software-Engineering/EFA-CAMverse?label=latest%20release&color=1e5aa8"></a>
  <a href="https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/LEBERT-Software-Engineering/EFA-CAMverse/total?label=downloads&color=0bb4cf"></a>
  <img alt="Windows 10 / 11, 64-bit" src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-555">
  <img alt="Free viewer – Pro features optional" src="https://img.shields.io/badge/viewer-free%20%C2%B7%20Pro%20optional-27d3a3">
  <a href="https://efacamverse.lebert.ai/"><img alt="Website" src="https://img.shields.io/badge/website-efacamverse.lebert.ai-1e5aa8"></a>
</p>

# <img src="assets/icon_camverse.png" width="36" alt="" valign="middle"> EFA CAMverse

**9 PCB/CAM formats. One view.**
EFA CAMverse opens Gerber X3, EAGLE, ODB++, IPC-2581, GenCAD, IPC-D-356, DXF, PADS and KiCad in a single native Windows tool – layers, stackup, drills, components and netlists at a glance, in 2D and 3D.

<table align="center">
  <tr>
    <td align="center"><h2>9</h2>formats, native</td>
    <td align="center"><h2>1</h2>tool, on-premise</td>
    <td align="center"><h2>100 %</h2>local &amp; secure</td>
  </tr>
</table>

> **New:** Gerber X/X2 + coordinates become Gerber X3 (for assembly) → [read more](#gerber-x3)

## Download

### [⬇ Download EFA CAMverse 2026 – latest release](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/latest)

| File | Purpose |
|---|---|
| [`EFA_CAMverse_2026_Setup_x64.exe`](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/latest/download/EFA_CAMverse_2026_Setup_x64.exe) | **Recommended.** Setup bundle including the Microsoft Visual C++ runtime. Interactive installer; upgrades an existing installation in place. |
| [`EFA_CAMverse_2026_x64.msi`](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/latest/download/EFA_CAMverse_2026_x64.msi) | Plain Windows Installer package for administrators and software deployment. Requires the Microsoft Visual C++ 2015–2022 x64 Redistributable. |
| `SHA256SUMS.txt` | SHA-256 checksums of the files above (attached to every release). |

**System requirements:** Windows 10 or Windows 11, 64-bit.

EFA CAMverse is free to use as a viewer – unlock advanced features whenever you need them. Native on Windows, your data stays local. The application occasionally points to other EFA SmartSuite products and checks for updates at startup.

### Windows SmartScreen

As EFA CAMverse has only just been released, Windows still shows a SmartScreen security prompt on first launch (“Windows protected your PC”). This is normal – the app is signed with an EV certificate and is safe. To run it:

**1 · More info** → **2 · Run anyway**

### Verifying the download

All binaries are signed with an Extended Validation code-signing certificate issued to **LEBERT Software Engineering GmbH & Co. KG**. Check the signature and the checksum in PowerShell and compare the hash with `SHA256SUMS.txt` of the release:

```powershell
Get-AuthenticodeSignature .\EFA_CAMverse_2026_Setup_x64.exe | Format-List Status, SignerCertificate
Get-FileHash .\EFA_CAMverse_2026_Setup_x64.exe -Algorithm SHA256
```

## Supported formats

**One viewer for every PCB/CAM format.** Open and view Gerber, ODB++, IPC-2581, KiCad and five more formats – from design to manufacturing inspection. EFA CAMverse reads each format natively, with no conversion and no cloud.

| | Format | |
|:---:|---|---|
| <img src="assets/fmt_gerber.png" width="40" alt="Gerber viewer"> | **Gerber X/X2/X3** | .gbr / .ger – RS-274X & Excellon drill data, incl. .gbrjob |
| <img src="assets/fmt_eagle.png" width="40" alt="EAGLE viewer"> | **EAGLE** | Open .brd & .sch files natively – no import |
| <img src="assets/fmt_odb.png" width="40" alt="ODB++ viewer"> | **ODB++** | View layers, nets & stackup |
| <img src="assets/fmt_ipc2581.png" width="40" alt="IPC-2581 viewer"> | **IPC-2581** | Open industry standard (DPMX) |
| <img src="assets/fmt_gencad.png" width="40" alt="GenCAD viewer"> | **GenCAD 1.4** <sub>UNIQUE</sub> | Assembly data – import & export |
| <img src="assets/fmt_ipc356.png" width="40" alt="IPC-D-356 viewer"> | **IPC-D-356** <sub>UNIQUE</sub> | Bare-board netlist & test data |
| <img src="assets/fmt_dxf.png" width="40" alt="DXF viewer"> | **DXF** | .dxf – mechanical & assembly (AutoCAD) |
| <img src="assets/fmt_pads.png" width="40" alt="PADS Layout viewer"> | **PADS Layout** <sub>UNIQUE</sub> | View .asc natively (Siemens/Mentor) |
| <img src="assets/fmt_kicad.png" width="40" alt="KiCad viewer"> | **KiCad** | Open .kicad_pcb & .kicad_pro |

<a id="gerber-x3"></a>
## Gerber X/X2 + coordinates = Gerber X3 (for assembly)

*New: for EMS providers.* Everyday EMS reality: the customer delivers classic Gerber data without component information – plus some pick & place file. EFA CAMverse merges both and adds the complete component layer you otherwise only get from Gerber X3.

- **Load the coordinate file – done:** EFA CAMverse automatically assigns pads, silkscreen outline and drill holes to every component.
- **No reformatting required:** EFA CAMverse detects the column layout, separators, decimal marks, units and board side by itself – even without a header row. You load the list as your customer sends it, be it from Altium, KiCad, EAGLE, …
- **Traceable, not a black box:** after every run a report shows which components were assigned reliably and which were not. If one sits wrong, you move it with two clicks in the image.
- **Just like real X3 from now on:** assembly views, variants, bill of materials and 3D are available, as if the data set had always known its components. The verified coordinates go out as CSV – for machine programming or straight back to your customer.

<table>
  <tr>
    <td align="center" valign="middle" width="26%">
      <img src="assets/fmt_gerber.png" width="48" alt=""><br>
      <b>Gerber X/X2</b> <code>.gbr</code><br>
      <sub>Layers, pads, drills – no component info</sub>
    </td>
    <td align="center" valign="middle"><h2>+</h2></td>
    <td align="center" valign="middle" width="30%">
      <b>Coordinates</b> <code>.csv / .txt</code>
      <pre>RefDes  X       Y      Rot
C12     12.70   45.10   90
R7      33.02   18.50    0
U3      58.42   27.94  270</pre>
      <sub>Pick &amp; place file from your CAD</sub>
    </td>
    <td align="center" valign="middle"><h2>=</h2></td>
    <td align="center" valign="middle" width="34%">
      <img src="assets/assembly_board.png" width="100%" alt="Populated board with labelled components – the result: Gerber X3 (for assembly)"><br>
      <b>Gerber X3 (for assembly)</b><br>
      <sub>Components, references, assembly views, BoM – the full X3 experience</sub>
    </td>
  </tr>
</table>

## Features – See. Verify. Manufacture.

One consistent feature set across every format – instead of a different tool for each one.

<table>
  <tr>
    <td width="33%" valign="top"><img src="assets/feat_layers.png" width="44" alt=""><br><b>Layers &amp; stackup</b><br>Toggle every layer, control transparency and read the full material build-up in the stackup pane.</td>
    <td width="33%" valign="top"><img src="assets/feat_3d.png" width="44" alt=""><br><b>3D view</b><br>View the board in space – with components as 3D bodies, rotate and zoom freely.</td>
    <td width="33%" valign="top"><img src="assets/feat_netlist.png" width="44" alt=""><br><b>Drills &amp; nets</b><br>Drill tables, netlist pane and bidirectional highlight – double-click to zoom to a net.</td>
  </tr>
  <tr>
    <td valign="top"><img src="assets/feat_components.png" width="44" alt=""><br><b>Assembly &amp; variants</b><br>Flexibly create assembly views – show or hide components to match the customer's variant with one click, with freely selectable labeling.</td>
    <td valign="top"><img src="assets/feat_x3.png" width="44" alt=""><br><b>Gerber X/X2 + coordinates = X3</b><br>Add external coordinate data to classic Gerber files – EFA CAMverse merges both into Gerber X3 (for assembly).</td>
    <td valign="top"><img src="assets/feat_exportfile.png" width="44" alt=""><br><b>Export &amp; manufacture</b><br>Export for manufacturing: images as PDF, PNG or JPG, coordinates and BoM as CSV.</td>
  </tr>
  <tr>
    <td valign="top"><img src="assets/feat_measure.png" width="44" alt=""><br><b>Measure &amp; inspect</b><br>Precise distance and geometry measurement – with bounding rectangle and centre of each component.</td>
    <td valign="top"><img src="assets/feat_export.png" width="44" alt=""><br><b>Convert formats &amp; GenCAD</b><br>Pass on imported data as GenCAD 1.4 – real conversion, not just viewing.</td>
    <td valign="top"><img src="assets/feat_offline.png" width="44" alt=""><br><b>Offline &amp; native</b><br>A native Windows application – no cloud, no upload. Your manufacturing data stays local.</td>
  </tr>
</table>

## Assembly drawing & variants

**Generate the assembly drawing yourself – exactly as production needs it.** EFA CAMverse does not display a supplied assembly drawing – it draws one from the data itself, component by component. That is precisely why your customer's variant can really be reproduced: whatever is not populated never appears in the first place.

- **Variant handling:** deselect and reselect components with one click – deselected parts disappear completely, along with body, pads and labelling. The delivered full population becomes the customer's variant, in 2D as well as 3D.
- **Selective labelling:** every component is automatically labelled with its reference – test points, fiducials or entire groups are suppressed by name pattern. Typeface and font size are yours to choose.
- **Colours to your specification:** board surface, edge, body, pads, pin-1 marker and labelling each have their own colour – pads, pin-1 and labelling can also be switched off entirely.
- **Add a layer:** place any layer you like – solder mask or drill map, for instance – over the assembly drawing in colour and semi-transparent.
- **Both sides:** top and bottom, each as its own assembly view.
- **Output:** export the assembly plan, coordinate data and bill of materials for production.

<table>
  <tr>
    <th width="50%">Full population</th>
    <th width="50%">Customer variant</th>
  </tr>
  <tr>
    <td><img src="assets/assembly_board.png" alt="Assembly drawing – full population"></td>
    <td><img src="assets/assembly_board_variant.png" alt="Assembly drawing – customer variant with unpopulated components removed"></td>
  </tr>
</table>

## 3D view

**The board in 3D – interactive and realistic.** One click switches from the layer view to a spatial representation: board, surfaces and components as a real 3D model – rotate and zoom freely.

<p align="center">
  <img src="assets/view3d_board.jpg" width="438" alt="EFA CAMverse 3D view: populated PCB panel with components as 3D models">
</p>

- **Realistically extruded board:** substrate, solder mask and surfaces just like the finished product.
- **Components as 3D bodies:** generated automatically – optionally with real 3D models from the downloadable model pack.
- **Assign models:** conveniently, with search and 3D preview in the assignment dialog.
- **Rotate and zoom freely:** components hidden by the variant disappear live in 3D too.

The optional **3D model pack** (KiCad 3D library models in VRML format, CC-BY-SA 4.0) is published as a separate [release](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases/tag/3dmodels-9.0.0); EFA CAMverse downloads and installs it from within the application.

## Why EFA CAMverse

**9 PCB/CAM formats. One application. One workflow.** One familiar way of working for every format: learn it once, then handle Gerber, ODB++, KiCad and six more formats the same way – all in a single application.

- **One way of working for everything** – learn it once, then operate every format identically: layers, stackup, measuring and export work the same everywhere.
- **Native, no detours** – open any format with no intermediate conversion and start working right away – no export-import back-and-forth between programs.
- **Formats side by side** – open different formats of the same project in one interface and view them together.
- **A bridge between formats** – read any of the 9 PCB/CAM formats and pass it on as GenCAD 1.4 – EFA CAMverse connects what otherwise stays separate.
- **One install, one update** – maintain one application instead of many separate tools – one update, one point of contact, all local.

| | What one tool gives you |
|---:|---|
| **9** | formats, one way of working |
| **1** | install instead of many tools |
| **0** | intermediate conversions needed |
| **3D** | the third dimension – inspect boards in space |
| **100 %** | offline & local – your data stays with you |

## Free viewer & Pro features

EFA CAMverse is free to use as a viewer – unlock advanced features whenever you need them.

**Pro features:**

1. create **assembly views** (top/bottom) with **configurable assembly print**
2. **export** coordinates & BoM as CSV, netlists
3. **convert** between PCB/CAM formats
4. … and much more

## About this repository

EFA CAMverse is proprietary, closed-source software by LEBERT Software Engineering. This repository does **not** contain source code – it is the public home for

- the **installer downloads** → [Releases](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/releases),
- the **[changelog](CHANGELOG.md)**,
- **bug reports and feature requests** → [Issues](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/issues).

## Support & feedback

- Found a bug or missing a feature? [Open an issue](https://github.com/LEBERT-Software-Engineering/EFA-CAMverse/issues/new/choose) – in English or German.
- Questions, licensing, confidential sample data: [EFA_CAMverse@lse.cc](mailto:EFA_CAMverse@lse.cc)
- Product website: [efacamverse.lebert.ai](https://efacamverse.lebert.ai/)

## Legal

<a href="https://lebert.org"><img src="assets/logo_lse.png" width="160" alt="LSE – LEBERT Software Engineering"></a>

EFA CAMverse is part of the **EFA SmartSuite** for electronics manufacturing – developed by [LEBERT Software Engineering](https://lebert.org).

© 2026 LEBERT Software Engineering GmbH & Co. KG. All rights reserved. Use of the software is subject to the [license terms](LICENSE.md). The software contains open-source components (OpenCV, pugixml, earcut.hpp, libzip, zlib) under their respective licenses; the optional 3D model pack contains KiCad library models under CC-BY-SA 4.0 – see [LICENSE.md](LICENSE.md).
All trademarks are the property of their respective owners.

[Imprint](https://lebert.org/impressum) · [Privacy policy](https://lebert.org/datenschutzerklaerung)
