# Obor — axonometrii ale spațiilor verzi și fondului construit

Versiune preliminară pentru proiect școlar, 17 octombrie 2026.

## Fișiere de consultat

- `Axonometrii_Obor_A3.pdf`: două pagini A3 peisaj, cu desen vectorial.
- `01_Axonometrie_generala.png` și `02_Axonometrie_interventie.png`: exporturi de înaltă rezoluție, 260 dpi.
- `Obor_analiza.qgz`: proiect QGIS, cu legături relative către `Obor_analiza.gpkg`. Păstrați cele două fișiere în același director.
- `Obor_volumetrie.blend`: model editabil Blender 4.3.2, cu două camere ortografice. Obiectele pot fi inspectate și modificate în Blender.
- `indicatori.json`: suprafețe în unități CAD pătrate și raportul suprafețelor GREEN disponibile. Aceste valori nu descriu inventarul verde real complet.

## Date și prelucrare

Surse primare: DWG-ul și PDF-ul furnizate de beneficiar. Amplasamentul este identificat de beneficiar ca București–Obor, în vecinătatea Gării Obor, cu reper Maps aproximativ 44.4505718, 26.1308242. Nu a fost efectuată o georeferențiere oficială a desenului.

DWG-ul AutoCAD 2018 a fost convertit într-o copie DXF folosind LibreDWG, revizia f860b0fb76d5f8effb5a70769a3389cb1e0308c8. Convertorul a raportat obiecte auxiliare necunoscute omise; nu se pretinde păstrarea completă a tuturor obiectelor proprietare CAD. Geometriile standard extrase au fost inspectate în plan și comparate cu PDF-ul.

Contururile de construcții provin din `Const_polygon`. Suprafețele coincidente și fragmentele adiacente au fost reunite; numărul de volume nu reprezintă numărul cadastral sau oficial al clădirilor. Modelul are 3.470 de volume în zona de studiu și contextul apropiat. Curțile interioare ale poligoanelor au fost păstrate în geometria editabilă și în acoperișurile desenate.

Limitele neagră și roșie din PDF au fost extrase vectorial și aliniate cu geometria CAD prin translație și scară uniformă. Reziduul median al corespondențelor apropiate utilizate la aliniere este aproximativ 0,04 unități CAD; acesta este un indicator intern de potrivire PDF–CAD, nu de precizie geografică.

## Vegetație

Layerul GREEN conține șapte contururi închise, plus două trasee deschise care nu au fost transformate în suprafețe. Contururile închise au fost validate geometric, reunite și decupate față de construcții. Beneficiarul a confirmat că reprezintă vegetație existentă.

Aceste suprafețe sunt în zona de studiu, în afara limitei roșii a intervenției. Inventarul este incomplet pentru întregul teritoriu. Nu au fost colorate arbitrar terenurile neconstruite. Layerul TREES este gol. Cei 28 de arbori din livrabile sunt reprezentări schematice, amplasate numai în suprafețele GREEN, cu înălțimi convenționale de circa 5–7 m și coroane de circa 2–3 m rază, în ipoteza unităților metrice. Pozițiile și dimensiunile nu sunt măsurate.

Nu sunt reprezentate suprafețe de apă.

## Înălțimi și reprezentare

Toate înălțimile clădirilor sunt estimări grafice, nu date reale verificate. A fost folosită o regulă morfologică simplă după aria și alungirea amprentei: în general 6, 9, 10 sau 12 m; unele corpuri alungite în afara frontului feroviar au fost reprezentate la 24 m. Corpurile din zona intervenției au fost limitate la maximum 9 m. Aceste reguli urmăresc lizibilitatea volumetrică pentru studiul școlar și pot clasifica greșit clădiri individuale; câmpul `inaltime_m` permite corecția lor în GIS. Nu se afirmă identificarea funcțiunilor sau regimurilor reale de înălțime.

Terenul a fost reprezentat plan. Proiecția este paralelă; nu există perspectivă și nu s-a exagerat separat axa verticală. Clădirile au fețe albe/neutre, muchii gri și tonuri discrete pe fațetele laterale. Axonometriile sunt o vedere generală și un detaliu al intervenției cu vecinătăți, nu o simulare a unor amenajări viitoare.

## Coordonate, unități și indicatori

Datele sunt păstrate într-un sistem local CAD. Nu s-a atribuit un cod EPSG neconfirmat. În Blender, originea a fost deplasată cu X=626950, Y=324600 pentru stabilitate numerică; aceste valori sunt salvate și în proprietățile obiectului principal.

Antetul DWG declară INSUNITS=2 (feet), dar dimensiunile apar compatibile cu un plan urban exprimat numeric în metri. Pentru modelarea școlară s-a adoptat provizoriu 1 unitate CAD = 1 m. Această ipoteză nu este verificată printr-o distanță de control. Suprafețele absolute nu trebuie utilizate pentru documentații tehnice sau bilanțuri oficiale. Săgeata N* urmărește +Y CAD; orientarea față de nordul geografic nu este confirmată.

Suprafețe calculate în coordonate CAD, rotunjite:

- studiu: 3.491.788 unități CAD²;
- intervenție: 107.960 unități CAD²;
- GREEN disponibil în studiu, după eliminarea suprapunerilor cu clădirile: 2.548 unități CAD²;
- raport GREEN disponibil / studiu: aproximativ 0,073%;
- GREEN disponibil în intervenție: zero intersecții.

**Raportul de 0,073% nu este ponderea reală a spațiilor verzi. Zero intersecții în intervenție înseamnă lipsa poligoanelor GREEN acolo, nu absența vegetației.** Arborii nu au fost adăugați la suprafețele verzi, evitând dubla numărare.

## Ce rămâne pentru o analiză completă a situației actuale

Interogările către serviciile Overpass au fost refuzate de proxy-ul de rețea în această sesiune. Nu au fost verificate integral date externe actuale, inventarul arborilor sau înălțimile clădirilor. Nu s-a folosit o imagine generată pentru a inventa geografie.

Pentru completarea analizei: ortofotoplan/imagine aeriană recentă cu drept de utilizare sau inventar GIS al vegetației, verificarea distanțelor/orientării cu repere și corectarea înălțimilor relevante. Aceste completări pot fi aplicate în fișierele editabile livrate.
