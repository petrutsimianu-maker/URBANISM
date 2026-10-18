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

## Plansa 2D — Plan2D_V03

In `livrabile/Plan2D_V03` se afla analiza in plan, fara arbori: verde inchis cu hasuri pline, constructii cu contur gri-antracit, parcele cu contur ocru-brun, legenda si diagrama circulara a bilantului. PDF vectorial A3, PNG 300 dpi, DXF 2D in metri, CSV si pachet ZIP cu SVG editabil.

Bilantul este orientativ si foloseste conventia agreata: suprafete vegetate si perimetre de parcuri/gradini, inclusiv aleile interne; constructiile si apa identificate sunt excluse. Spatiile verzi cartografiate nu reprezinta un inventar oficial exhaustiv. Aria studiului: 349,18 ha; verde cartografiat: 11,56 ha (3,31%); construit la sol: 86,89 ha (24,89%); alte suprafete: 71,80%.
