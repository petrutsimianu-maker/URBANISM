# Obor — axonometrii V02, corectarea inventarului vegetal

17 octombrie 2026. Studiu școlar. Această versiune înlocuiește planșele V01, care foloseau numai cele șapte poligoane închise din GREEN și omiteau o parte importantă din datele DWG.

## Ce s-a corectat

Au fost inspectate și definițiile de blocuri, nu numai entitățile din model space. Blocurile Block_1–Block_8 conțin o hartă vectorială stocată în desen, cu contururi de construcții și simboluri circulare/elliptice verzi în Block_2. Blocurile nu erau inserate ca obiecte active în model space. Folosirea lor necesită extragere și aliniere separată; nu se presupune că sunt o bază de arbori măsurați.

Harta recuperată a fost corelată cu planul pe sute de contururi. Transformarea aproximativă din coordonatele blocurilor în CAD este o similitudine: X_CAD=a*x−b*y+tx, Y_CAD=b*x+a*y+ty, cu parametrii salvați în block_registration.json. Acoperă aproximativ 39,6% din zona de studiu și întregul contur al intervenției. Circa 7.295 de simboluri au fost păstrate în studiu/context după eliminarea centrelor care cad în amprentele clădirilor; 6.238 dintre acestea au centrul în zona de studiu. Dimensiunile coroanelor și înălțimile sunt convenționale.

Accesul la API-ul OpenStreetMap a permis completarea în întregul teritoriu de studiu a parcurilor, grădinilor și suprafețelor vegetate cartografiate. Au fost selectate 161 de geometrii OSM care intersectează studiul sau contextul de 100 m; o parte intersectează numai contextul. Sunt prezente, între altele, Parcul Obor, Parcul Păsărari, Parcul Ziduri Moși și Parcul Lunca Florilor. Au fost adăugate 213 puncte de arbori OSM care nu dublează simbolurile CAD apropiate. Totalul reprezentat în studiu/context este 7.508 simboluri de arbori.

## Surse și categorii

- DWG și PDF furnizate de beneficiar: geometria clădirilor, drumurilor și căilor ferate; limitele studiului și intervenției; GREEN; simbolurile vegetale recuperate din blocuri.
- OpenStreetMap, extragere 17.10.2026 prin https://www.openstreetmap.org/api/0.6/map: poligoane leisure=park/garden/nature_reserve/recreation_ground, landuse=grass/forest/meadow/orchard/allotments/village_green, natural=wood/grassland/scrub/heath și puncte natural=tree. Interogările acoperă fereastra 26.11–26.17 E, 44.43–44.475 N. Relațiile multipolygon complete au fost asamblate; o relație incompletă din extragerea extinsă nu a fost folosită ca geometrie completă. Nu s-a presupus că lipsa unui obiect în OSM înseamnă absența sa în teren.
- © OpenStreetMap contributors. Date OSM disponibile sub Open Database License (ODbL): https://www.openstreetmap.org/copyright și https://opendatacommons.org/licenses/odbl/1-0/ . ID-urile și tagurile sursă sunt păstrate în GeoPackage pentru verificare.

Verdele mai închis reprezintă suprafețe cartografiate ca vegetate, iar verdele deschis perimetre de parcuri/grădini. **Perimetrul unui parc include și alei sau platforme pavate; nu este echivalent cu o suprafață exclusiv înierbată.** Amprentele construite și apa identificată în DWG au fost eliminate din suprafețele colorate. Apa nu are umplere sau simbolizare tematică.

Coroanele arborilor sunt simboluri convenționale, nu diametre inventariate în teren. Punctele CAD sunt păstrate prioritar; punctele OSM aflate la mai puțin de 4 m de un simbol recuperat nu au fost dublate. Simbolurile CAD reprezintă informație stocată în fișier, cu dată de referință necunoscută. Nu se afirmă că fiecare arbore mai există astăzi sau că toți arborii din teritoriu sunt reprezentați.

## Aliniere și unități

Datele OSM WGS84 au fost proiectate în Stereo 70, EPSG:3844, cu ordinea XY=easting,northing. Corelarea cu construcțiile CAD a permis o translație fără schimbare de scară sau rotație:

X_CAD = X_Stereo70 + 36111.871349
Y_CAD = Y_Stereo70 − 4005.195549

Controlul pe 876 de contururi compatibile a dat un reziduu median între centroizi de aproximativ 1,56 m și percentila 90 de 3,60 m. Diferențele includ schimbări ale construcțiilor și diferențe de digitizare; aceste valori nu sunt o certificare topografică. La nivelul studiului școlar, potrivirea susține utilizarea scării metrice 1:1, în pofida antetului INSUNITS=2 din DWG. Săgeata N* indică nordul grilei Stereo70.

GeoPackage și proiectul QGIS V02 sunt în EPSG:3844, după eliminarea translației locale CAD. Modelul Blender păstrează originea CAD deplasată cu (626950,324600) pentru stabilitate numerică. PDF-ul folosește aceleași geometrii în coordonate locale. Fișierul osm_registration.json păstrează transformarea și controalele de aliniere.

## Fond construit

Clădirile provin prioritar din Const_polygon, cu geometriile adiacente/coincidente reunite. Sunt 3.470 de volume în studiu și context; acestea nu sunt un inventar cadastral de imobile.

Înălțimile nu au fost măsurate și nu au fost verificate pentru fiecare clădire. Sunt estimate morfologic după aria și alungirea amprentei, în general 6, 9, 10 sau 12 m; unele corpuri alungite au 24 m, iar cele din intervenție au fost limitate la 9 m. Regulile pot clasifica greșit corpuri individuale și servesc doar lecturii volumetrice școlare. Câmpul inaltime_m permite corecții în GIS. Clădirile sunt albe, cu fețe neutre și muchii discrete; terenul este plan.

## Indicatori și limite

Indicatorii au fost recalculați în indicatori.json. Suprafețele de land cover și perimetrele de parcuri sunt raportate separat și fără dublă numărare între aceste două grupuri. Coroanele simbolice nu se adaugă suprafețelor la sol. Nu se calculează o pondere oficială sau exhaustivă a spațiilor verzi reale: sunt disponibile numai geometriile identificate în sursele folosite.

Inventarul vegetației între blocuri, al grădinilor private și al arborilor poate rămâne incomplet, mai ales în afara acoperirii blocurilor CAD. Pentru o inventariere exhaustivă ar fi necesare ortofotoplanuri recente și/sau un inventar local al spațiilor verzi, urmate de verificare vizuală sau în teren. În această versiune nu au fost inventate suprafețe verzi în toate parcelele neconstruite.

## Utilizare

- Axonometrii_Obor_A3.pdf: două planșe vectoriale A3 peisaj; aceleași vederi au exporturi PNG.
- Obor_analiza.qgz și Obor_analiza.gpkg: se păstrează în același folder; proiectul utilizează căi relative și include extrudarea 3D a clădirilor după inaltime_m.
- Obor_volumetrie.blend: Blender 4.3.2, două camere ortografice, clădiri și vegetație editabile. Arborii sunt grupați în mesh-uri pentru performanță; pozițiile și proveniența individuală sunt în GeoPackage și tree_provenance.json.
