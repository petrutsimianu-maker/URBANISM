# URBANISM — Obor

## Planuri 2D actualizate: V04

Folositi **livrabile/Plan2D_V04** pentru analiza 2D actuala. Au fost completate zonele indicate de beneficiar: V1 Gara Obor / Caminului, V2 Eufrosin Poteca / Murgescu / Baicului, V3 Parcul Hobita. PDF-ul contine plansa generala si trei detalii. Pachetul ZIP include PDF/PNG/SVG, DXF in metri, centralizator CSV/PDF si date GIS.

DXF-ul are layer separat **VERDE_SUPRAFETE**, cu 121 de coduri si arii ale contururilor verzi independente; hasurile sunt pe VERDE_PLIN. Etichetele sunt valori la export, nu campuri dinamice. Aria verde cartografiata V04: 141.572,83 m2 (14,16 ha), 4,05% din studiu. Suprafetele sunt orientative, potrivit conventiei agreate pentru parcuri; completarile din capturi nu sunt o ridicare topografica. Consultati CITESTE_MA.txt.

## Axonometrii: V02

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

## Incadrarea functionala orientativa — schema beneficiarului

`livrabile/Incadrare_V04` contine harta si tabelul tuturor celor 121 de contururi V04, analizate dupa cele trei categorii furnizate de beneficiar. Rezultat: 47 compatibile probabil cu categoria 1, 24 cu categoria 3, doua contururi mixte si 48 neconfirmate. Nu s-a identificat o categorie 2 confirmata in inventarul actual. Nu reprezinta clasificare juridica oficiala CATUC; forma normativa nu a fost verificata, iar datele hartii nu certifica accesul/proprietatea. Planul si bilantul V04 nu au fost modificate. Raportul explica motivele si verificarile necesare, iar CSV-ul include sursele OSM.
