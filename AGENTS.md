# Pravidlá pre spracovanie poznámok z elektrotechniky

Toto repo uchováva zápisky zo školy. Najvyššou prioritou je vernosť tomu, čo autor napísal. Zápisky neslúžia ako miesto na samostatné opravy učiva.

## Štruktúra

- `povodne/` obsahuje nedotknuté kópie súborov presne v stave pri prijatí. Je to miestna záloha aj súčasť histórie Gitu.
- `hodiny/` obsahuje jeden súbor za každú hodinu. Opravuje sa v ňom iba diakritika a Markdown zvýraznenie. Nadpisy a pôvodné poradie viet a bodov zostávajú zachované.
- `ucivo/` obsahuje priebežne usporiadané učivo podľa tém. Každý fakt tu musí mať pôvod v `hodiny/`. Súbory odkazujú na zdrojovú hodinu.
- `NEJASNOSTI.md` zaznamenáva miesta, ktoré môžu byť preklepom, nezrozumiteľné alebo vecne nesprávne. Tento súbor nie je opravou poznámok.

## Postup pri novej hodine

1. Zisti, ktoré nové súbory autor pridal, a prečítaj aktuálny stav repozitára. Existujúce zmeny používateľa neprepisuj.
2. **Pred akoukoľvek úpravou** skopíruj každý nový pôvodný súbor do `povodne/` ako bajtovo identickú kópiu. Použi jeho pôvodný názov, ak je voľný. Ak existuje, zvoľ nový jednoznačný názov bez prepísania staršej zálohy.
3. Porovnaj SHA-256 pôvodného súboru a zálohy. Ak sa nezhodujú, zastav úpravy daného súboru.
4. Z kópie vytvor `hodiny/hodinaN.md`. Zachovaj všetky vety, slová, čísla, vzorce, jednotky, príklady, negácie, poradie a význam. Smieš doplniť alebo opraviť slovenskú diakritiku a upraviť iba Markdown zvýraznenie, teda `**...**` alebo `*...*`. Neopravuj pravopis bez diakritiky, gramatiku, interpunkciu, odborné názvy ani faktické chyby. Nepridávaj vysvetlenia. Ak je doplnenie diakritiky významovo nejednoznačné, zachovaj pôvodný zápis a zaznač nejasnosť do `NEJASNOSTI.md`.
5. Zapracuj všetky pôvodné tvrdenia do `ucivo/`. Môžeš pridať nadpisy, rozdeliť text do tematických súborov, upraviť odseky, odrážky, zalomenie, interpunkciu a zvýraznenie pre čitateľnosť. Zachovaj každý pôvodný fakt, číslo, jednotku, príklad, podmienku aj kvalifikáciu. Nemeň význam. Neskracuj obsah tak, aby sa stratila informácia. Nedopĺňaj učivo z pamäti ani z internetu.
6. Pri každej téme v `ucivo/` uveď odkaz na príslušnú hodinu. Ak sa téma objaví vo viacerých hodinách, uveď všetky zdroje. Ak si zdroje odporujú, obidve tvrdenia ponechaj s pôvodom a konflikt zaznač do `NEJASNOSTI.md`.
7. Urob kontrolu pokrytia. Prejdi každý bod v novom súbore v `hodiny/` a nájdi ho v `ucivo/`. Skontroluj najmä čísla, jednotky, znamienka, príklady a slová ako „nie“, „iba“, „vždy“ a „nikdy“. Porovnaj zmeny v `hodiny/` s `povodne/`; mimo diakritiky a zvýraznenia sa nesmie zmeniť obsah.
8. V `README.md` udržuj stručný zoznam hodín a tém. Po kontrole urob commit s opisom pridanej hodiny. Push na súkromné GitHub repo urob, ak je dostupné prihlásenie a používateľ tento krok autorizoval.

## Hranice

- Chybu v zápiskoch neopravuj podľa vlastných vedomostí, ani keď si si istý. Zapíš návrh na preverenie do `NEJASNOSTI.md` s odkazom na zdroj.
- Nikdy spätne nemeň súbory v `povodne/`. Nová verzia vstupu potrebuje novú zálohu.
- Nezlievaj dve rôzne tvrdenia do jedného, ak by sa tým stratil ich pôvod alebo odlišné znenie.
- Ak používateľ výslovne požiada o vecnú opravu, rieš ju ako samostatnú úlohu. Nezamieňaj opravené učivo za verný prepis bez jasného označenia.
- Pri nejasnom texte radšej zachovaj doslovné znenie a opýtaj sa autora, než aby si hádal.
