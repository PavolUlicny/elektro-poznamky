# Pravidlá pre spracovanie poznámok z elektrotechniky

Toto repo uchováva zápisky zo školy. Najvyššou prioritou je vernosť tomu, čo autor napísal. Zápisky neslúžia ako miesto na samostatné opravy učiva.

**Do `povodne/` patria výhradne bajtovo identické kópie pôvodných poznámok autora. Sú 100 % nedotknuteľné. Nie je v nich povolená žiadna úprava obsahu ani formy, ani oprava jediného znaku.**

## Štruktúra

- `povodne/` obsahuje nedotknuté kópie súborov presne v stave pri prijatí. Je to miestna záloha aj súčasť histórie Gitu.
- `hodiny/` obsahuje jeden súbor za každú hodinu. Opravuje sa v ňom diakritika a Markdown zvýraznenie; grécke písmená a matematické zápisy sa upravujú podľa pravidiel nižšie. Nadpisy a pôvodné poradie viet a bodov zostávajú zachované.
- `ucivo/` obsahuje priebežne usporiadané učivo podľa tém. Každý fakt tu musí mať pôvod v `hodiny/`. Súbory odkazujú na zdrojovú hodinu.
- `obrazky/hodinaN/` obsahuje obrázky a náčrty na vloženie do príslušnej hodiny a tém učiva. Ich nedotknuté originály sa zálohujú do `povodne/obrazky/hodinaN/`.
- `NEJASNOSTI.md` zaznamenáva miesta, ktoré môžu byť preklepom, nezrozumiteľné alebo vecne nesprávne. Tento súbor nie je opravou poznámok.

## Úplná nedotknuteľnosť `povodne/`

- Každý súbor do `povodne/` ulož priamym kopírovaním pôvodného vstupného súboru. Neprepisuj ho ručne ani ho neregeneruj z jeho obsahu. Kópia musí byť bajtovo identická so zdrojom v okamihu prijatia.
- Nemeň absolútne nič: text, diakritiku, preklepy, interpunkciu, medzery, zalomenia riadkov, kódovanie, formátovanie, grécke písmená, vzorce, jednotky ani príklady. Aj nesprávny či neúplný zápis musí zostať presne pôvodný. Žiadna výnimka pre úpravu zápisu sa na `povodne/` nevzťahuje.
- Nevkladaj do pôvodných súborov komentáre, upozornenia, odkazy, vysvetlenia ani opravy z chatu, internetu, učebníc, poznámok spolužiaka či vlastných vedomostí. Nejasnosti patria do `NEJASNOSTI.md` a spracované verzie do `hodiny/` a `ucivo/`.
- Existujúce zálohy nikdy neprepisuj, neupravuj ani nemaž. Ak autor dodá upravenú verziu vstupu, ulož ju ako novú samostatnú zálohu bez zmeny staršej verzie.
- Po skopírovaní over zhodu SHA-256 zdroja a kópie. Samotné vytvorenie spracovanej verzie v `hodiny/` alebo `ucivo/` nesmie nijako zmeniť zálohu v `povodne/`.

## Postup pri novej hodine

1. Zisti, ktoré nové súbory autor pridal, a prečítaj aktuálny stav repozitára. Existujúce zmeny používateľa neprepisuj.
2. **Pred akoukoľvek úpravou** skopíruj každý nový pôvodný súbor do `povodne/` ako bajtovo identickú kópiu. Použi jeho pôvodný názov, ak je voľný. Ak existuje, zvoľ nový jednoznačný názov bez prepísania staršej zálohy.
3. Porovnaj SHA-256 pôvodného súboru a zálohy. Ak sa nezhodujú, zastav úpravy daného súboru.
4. Z kópie vytvor `hodiny/hodinaN.md`. Zachovaj všetky vety, slová, čísla, vzorce, jednotky, príklady, negácie, poradie a význam s výnimkou povolených zmien zápisu uvedených nižšie. Smieš doplniť alebo opraviť slovenskú diakritiku, upraviť Markdown zvýraznenie, teda `**...**` alebo `*...*`, a previesť grécke písmená, vzorce, jednotky a výpočty do matematickej syntaxe podľa nasledujúcej sekcie. Za povolenú opravu diakritiky v `hodiny/` aj `ucivo/` sa považuje aj zmena `e` alebo `a` na `ä`, ak je z kontextu jednoznačné, že tam patrí, napríklad `napetie` alebo `napatie` na `napätie`. Táto výnimka sa nevzťahuje na nedotknuteľné zálohy v `povodne/`. Dodané obrázky vlož podľa sekcie „Obrázky a náčrty“ bez zmeny poradia pôvodného textu. Neopravuj ostatný pravopis, gramatiku, interpunkciu, odborné názvy ani faktické chyby. Nepridávaj vysvetlenia. Ak je doplnenie diakritiky alebo prevod zápisu významovo nejednoznačný, zachovaj pôvodný zápis a zaznač nejasnosť do `NEJASNOSTI.md`.
5. Zapracuj všetky pôvodné tvrdenia do `ucivo/`. Môžeš pridať nadpisy, rozdeliť text do tematických súborov, upraviť odseky, odrážky, zalomenie, interpunkciu a zvýraznenie pre čitateľnosť. Použi aj pravidlá pre grécke písmená a matematický zápis uvedené nižšie. Zachovaj každý pôvodný fakt, číslo, jednotku, príklad, podmienku aj kvalifikáciu. Nemeň význam. Neskracuj obsah tak, aby sa stratila informácia. Nedopĺňaj učivo z pamäti ani z internetu.
6. Pri každej téme v `ucivo/` uveď odkaz na príslušnú hodinu. Ak sa téma objaví vo viacerých hodinách, uveď všetky zdroje. Ak si zdroje odporujú, obidve tvrdenia ponechaj s pôvodom a konflikt zaznač do `NEJASNOSTI.md`.
7. Urob kontrolu pokrytia. Prejdi každý bod v novom súbore v `hodiny/` a nájdi ho v `ucivo/`. Skontroluj najmä čísla, jednotky, znamienka, príklady a slová ako „nie“, „iba“, „vždy“ a „nikdy“. Porovnaj zmeny v `hodiny/` s `povodne/`; povolené sú iba zmeny diakritiky, zvýraznenia, prevod zápisu podľa nasledujúcej sekcie a vloženie dodaných obrázkov podľa sekcie „Obrázky a náčrty“. Pri prevode vzorcov over, že sa nezmenili hodnoty, operácie, zátvorky, exponenty, indexy, jednotky ani význam symbolov. Skontroluj aj pokrytie dodaných obrázkov a funkčnosť ich relatívnych ciest.
8. V `README.md` udržuj stručný zoznam hodín a tém. Po kontrole urob commit s opisom pridanej hodiny. Push na súkromné GitHub repo urob, ak je dostupné prihlásenie a používateľ tento krok autorizoval.

## Grécke písmená a matematický zápis

Tieto pravidlá platia pri spracovaní do `hodiny/` aj `ucivo/`. Pôvodné vstupné súbory ani zálohy v `povodne/` podľa nich neupravuj.

- Grécke písmená používané ako značky zapisuj ich znakmi, napríklad ρ, κ, α a Ω. V matematickom zápise použi zodpovedajúce príkazy LaTeXu, napríklad `\rho`, `\kappa`, `\alpha` a `\Omega`. Slovné označenia ako „ró“, „kappa“, „alfa“ alebo „omega“ ponechaj, ak je účelom vety uviesť názov alebo výslovnosť písmena. Rozlišuj veľké a malé písmená.
- Vzorce a matematické výrazy zapisuj pomocou matematickej syntaxe LaTeXu podporovanej GitHub Markdownom. Krátky výraz v texte ohranič `$...$`. Samostatný vzorec alebo postup výpočtu ohranič `$$` na samostatných riadkoch. Vzorce nenechávaj ako obyčajný text ani v kódových blokoch.
- Používaj zlomky `\frac{...}{...}`, mocniny `^{...}`, indexy `_{...}` a násobenie `\cdot` tam, kde vyjadrujú pôvodný zápis. Napríklad `R = ró * (l / S)` prepíš na `$R = \rho \frac{l}{S}$` a `kappa = 1 / ró` na `$\kappa = \frac{1}{\rho}$`.
- Jednotky vo vzorcoch zapisuj stojatým písmom pomocou `\mathrm{...}` s medzerou medzi hodnotou a jednotkou, napríklad `$3\,\mathrm{A/mm^2}$` alebo `$\Omega\cdot\mathrm{m}$`. Zachovaj pôvodnú jednotku aj predponu; samotné formátovanie neoprávňuje na prevod jednotiek ani opravu ich významu.
- Pri príkladoch zachovaj zadanie, dané hodnoty, hľadané veličiny, všetky pôvodné kroky a výsledok. Výpočet oddeľ od zadania do matematického bloku; viac nadväzujúcich rovností môžeš zarovnať prostredím `aligned`. Príklad má byť čitateľný ako zadanie a postup výpočtu, nie ako súvislý odsek obyčajného textu. Nedopĺňaj chýbajúce kroky, hodnoty ani riešenia, ktoré autor neuviedol.
- Prevod do matematickej syntaxe mení iba zápis. Neopravuj pri ňom odborné chyby a nehádaj nejednoznačné symboly. Také miesto ponechaj podľa zdroja a zaznač do `NEJASNOSTI.md`.

## Obrázky a náčrty

- Obrázky dodané autorom sú súčasťou pôvodných poznámok. Pred spracovaním každý z nich zálohuj priamym kopírovaním do `povodne/obrazky/hodinaN/` a over zhodu SHA-256 so vstupom. Zachovaj pôvodný názov súboru; pri kolízii použi nový jednoznačný názov bez prepísania staršej zálohy. Úplná nedotknuteľnosť `povodne/` platí aj pre obrázky.
- Kópie na zobrazenie ulož do `obrazky/hodinaN/` s krátkymi opisnými názvami bez medzier a diakritiky, napríklad `uzol.png`, `vetva.png`, `slucka.png` a `svorka.png`. Ponechaj pôvodný formát a obsah. Bez výslovnej požiadavky obrázky neorezávaj, neprekresľuj, neotáčaj, nekomprimuj ani inak neupravuj. Predvolená kópia na zobrazenie musí byť bajtovo identická so zálohou. Vyžiadanú upravenú verziu ulož osobitne a zachovaj jej väzbu na originál.
- Pred vložením si obrázok prezri a over jeho priradenie k hodine a téme. Neurčuj obsah iba podľa názvu súboru. Ak priradenie nie je jasné, nehádaj a zaznač nejasnosť do `NEJASNOSTI.md`.
- V `hodiny/hodinaN.md` vlož náčrt hneď za príslušnú definíciu, vzorec alebo príklad. V `ucivo/` ho vlož priamo k zodpovedajúcej téme a uveď odkaz na zdrojovú hodinu. Pri opakovanom použití odkazuj na rovnaký súbor v `obrazky/`; nevytváraj zbytočné duplikáty.
- Používaj Markdown obrázky s relatívnou cestou od konkrétneho súboru, napríklad `![Náčrt uzla](../obrazky/hodina3/uzol.png)`. Cesty musia fungovať po naklonovaní repozitára aj na GitHube. Nepoužívaj absolútne miestne cesty ani dočasné či externé adresy. Alternatívny text má stručne pomenovať dodaný obrázok bez pridania odborného výkladu.
- Zachovaj všetky dodané náčrty, ich značky, hodnoty a označenia. Nenahrádzaj ich vlastnou schémou, obrázkom z internetu ani textovým prepisom. Prípadné chyby alebo rozpor s textom zaznač do `NEJASNOSTI.md`; samotný obrázok neopravuj.
- Pri kontrole over, že každý dodaný obrázok má nezmenenú zálohu a je vložený pri príslušnom obsahu. Otvor spracovaný Markdown v náhľade a skontroluj načítanie obrázkov aj čitateľnosť označení. Do commitu zahrň Markdown, zálohy aj všetky odkazované obrázky.

## Hranice

- Chybu v zápiskoch neopravuj podľa vlastných vedomostí, ani keď si si istý. Zapíš návrh na preverenie do `NEJASNOSTI.md` s odkazom na zdroj.
- Nikdy spätne nemeň súbory v `povodne/`. Nová verzia vstupu potrebuje novú zálohu.
- Nezlievaj dve rôzne tvrdenia do jedného, ak by sa tým stratil ich pôvod alebo odlišné znenie.
- Ak používateľ výslovne požiada o vecnú opravu, rieš ju ako samostatnú úlohu. Nezamieňaj opravené učivo za verný prepis bez jasného označenia.
- Pri nejasnom texte radšej zachovaj doslovné znenie a opýtaj sa autora, než aby si hádal.
