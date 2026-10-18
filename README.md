# URBANISM — Obor

## Versiunea curentă: V02

Folosiți fișierele din **livrabile/V02**. Această versiune corectează inventarul vegetal insuficient din prima versiune.

- `Obor_V02.pdf`: două planșe axonometrice A3, cu vegetație recuperată din blocurile DWG și completări OpenStreetMap.
- `01_Axonometrie_generala.png` și `02_Axonometrie_interventie.png`: previzualizări.
- `Obor_V02_editabil.zip`: PDF/PNG, QGIS, GeoPackage și Blender.
- `NOTA_METODOLOGICA.md`: sursele, alinierea și limitele modelului.

Date OSM: © OpenStreetMap contributors, ODbL, https://www.openstreetmap.org/copyright . Înălțimile clădirilor și coroanele arborilor rămân estimate/simbolice. Inventarul vegetației nu este exhaustiv. Perimetrele parcurilor includ și alei.

Pentru descărcare, deschideți fișierul în GitHub și apăsați **Download raw file**. Fișierele inițiale din `livrabile` sunt păstrate pentru istoric; V02 le înlocuiește pentru utilizarea curentă.

## Import Archicad 26

In `livrabile/Archicad26` se afla exportul IFC2x3 si pachetul ZIP pentru Archicad 26. ZIP-ul include modelul complet, o varianta numai cu cladiri, un plan DXF 2D in metri si instructiuni. Import: **File → Open → Open**, selectati fisierul IFC; dupa import salvati ca PLN. Sunt volume IFC generice, nu elemente constructive native BIM. Schema si geometria tuturor elementelor au fost verificate cu IfcOpenShell; importul in aplicatia Archicad nu a fost testat in mediul cloud.
