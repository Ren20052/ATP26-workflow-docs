## 5. Markdown - perolaki označiteljski jezik za vođenje bilježaka

Obsidian koristi **Markdown** – jednostavni označiteljski jezik – za formatiranje tekstualnih bilješki. To znači da svaka bilješka u pozadini postoji kao obična `.md` tekst datoteka s Markdown sintaksom. Markdown je vrlo intuitivan i jednostavan za naučiti; sastoji se od oznaka unutar teksta koje označavaju naslove, podebljanja, popise itd. Navodimo neke od najčešćih Markdown oznaka koje se koriste pri izradi bilješki:
- **Naslovi:** Koristite znak `#` za naslov na početnoj razini. Više `######` (do 6) daju podnaslove nižih razina.  
    _Primjer:_ `# Naslov 1` za glavni naslov, `## Podnaslov` za podnaslov itd.
- **Podebljane i kurziv:** Tekst okružen dvostrukim zvjezdicama `**` se prikazuje **podebljan**, a tekst u jednostrukim zvjezdicama `*` se prikazuje u _kurzivu_.  
    _Primjeri:_ `**važan pojam**` prikazuje **važan pojam**, a `*istakni ovo*` prikazuje _istakni ovo_.
- **Popisi:** Za nabrajanje ili nenumerirane popise koristite crticu `-` ili zvjezdicu `*` na početku retka. Za numerirane popise koristite brojke s točkom (npr. `1.`).  
    _Primjer:_

```markdown
- Prva stavka  
- Druga stavka  
    - Podstavka (uvučena s 4 razmaka ili tab)  

1. Prva stavka
2. Druga stavka
	1. Dodatna stavka
	2. Dodatna stavka
	3. ...
```
- **Linkovi:** Postoje **vanjski ** i **unutarnji linkovi**. Za vanjske linkove koristimo sljedeću sintaksu `[tekst](URL)`, npr. `[Obsidian web](https://obsidian.md)`. Unutarnje poveznice na druge bilješke (tzv. **wiki linkovi**) pišu se u dvostrukim uglatim zagradama `[[ ... ]]`. Kod upisivanja `[[` Obsidian će ponuditi *autocomplete* za postojeće bilješke. Ako upišete naziv koji ne postoji i zatvorite zagradu, kreirat će se nova bilješka s tim nazivom. Ovo je ključno za povezivanje bilješki unutar vaulta.
- **Citati/blokovi teksta:** Veći citati ili napomene mogu se istaknuti znakom `>` na početku retka, čime tekst postaje citatni blok.
- **Blokovi koda:** Za umetanje koda ili pseudo-koda, koristite trostruke backtick oznake \`\`\` (tzv. _fenced code block_). Obsidian podržava i isticanje sintakse za kod, ali za to vam je potreban plugin pod nazivom *Code Styler* a pronaći ćete ga pod "Community plugins".

```python
Code Styler i prikaz sintakse računalnog koda
a = 2
b = 2
c = a*b
print(c)
4
```

- **Slike:** Umetanje slike koristeći sintaksu `![[naziv-slike.png]]` ako je datoteka slike unutar spremišta, ili `![Alt tekst](URL_do_slike)` za online slike. (Napomena: Obsidian također ima posebnu funkciju _drag-and-drop_ za slike – ako sliku povučete u bilješku, bit će spremljena u spremište i umetnuta u bilješku.)
- **Transkluzije**: Obsidian omogućuje "umetanje" ili "ugrađivanje" (engl. "embedding") jedne ili više bilješki unutar druge. Kada se izvorna bilješka ažurira, promjene se automatski odražva u svim bilješkama u koje je uključena. Da bi se cijela bilješka ugradila u drugu, koristimo sljedeću sintaksu: `![[Naziv druge bilješke]]`

> [!TIP] Osnovna i napredna Markdown sintaksa
> Ovo su osnovne oznake dovoljne za većinu bilješki. Više informacija o načinima korištenja Markdowna u Obsidianu možete pronaći unutar [Obsidian Help](https://help.obsidian.md/syntax). 

Tijekom pisanja u **Edit modu**, tekst će sadržavati ove oznake, a prelaskom u **Preview** vidjet ćete lijepo formatiran tekst (naslovi uočljiviji, popisi poredani, slike prikazane itd.). Uz malo prakse, počet ćete koristiti _Live Preview_ gdje su neke oznake odmah formatirane dok tipkate (Obsidian v1.0+ omogućuje to). Predlažem da odmah isprobate: **stvori novu bilješku** klikom na ikonu “New Note” (ili tipka `Ctrl+N`), nazovite je primjerice “Markdown vježba” i pokušajte u nju upisati nekoliko gore navedenih elemenata (naslov, podnaslov, podebljanu riječ, popis od par stavki, i jedan wiki link na bilješku koju još niste stvorili, npr. `[[Nova bilješka]]`). Potom uključite _Preview_ da vidite rezultat formatiranja.

## 6. Struktura vaulta i organizacija bilješki u Obsidianu

Sada ćemo postaviti osnovnu **strukturu unutar spremišta** kako bismo isprobali prethodno navedena načela organizacije bilješki (počinjemo kao  “arhitekti”). Ova struktura nije obvezna – Obsidian ne zahtijeva da bilješke budu u posebnim mapama – ali za početak nam može pomoći da napravimo dedicirana mjesta za različite vrste sadržaja. Inicijalnu strukturu možete kasnije uvijek prilagoditi vlastitim potrebama, stilu i očekivanjima od samog sustava.

Predložena inicijalna struktura vaulta (folderi na root razini):
- `00 Inbox` – _privremeno spremište_ za nove bilješke ("hladnjak") ili ulazne informacije koje još niste uredili ili rasporedili. Ovdje možete brzo ubaciti svaku novu ideju, misao ili bilješku koju ćete eventualno kasnije razvrstati.
- `01 Projekti` – konkretni projekti ili zadaci na kojima ste aktivni. Unutar ovog foldera možete imati pod-foldere ili bilješke za svaki aktivni projekt. (Npr. jedan za nastavni projekt, jedan za istraživački rad kojeg pišete, itd.)
- `02 Područja` – odgovornosti, odnosno teme ili domene od trajnog interesa. Npr. “Metodika nastave”, “Strojno učenje”, “Upravljanje timom” – ovisno čime se kontinuirano bavimo. Unutar toga mogu ići bilješke vezane uz tu domenu.
- `03 Resursi` – opći referentni materijali, bilješke koje nisu "strogo" vezane za jedan projekt nego su općekorisne. Tu će recimo ići većina literaturnih bilješki, koncepti, sažeci knjiga, tutorijali, ideje za buduće radove i sl. (osobe koje prakticiraju Zettelkasten pristup vrlo često sve drže u jednom folderu i oslanjaju se na stvaranje poveznica među različitim vrstama bilješki)
- `04 Arhiv` – ovdje premještamo bilješke/projekte koje više nisu aktivni. (npr. završene projekte možemo prebaciti ovdje radi čuvanja; održana predavanja možemo također spremiti na ovo mjestu iz kojeg se jednostavno mogu ponovno aktivirati i uključiti u neki aktivni zadatak)
- `Attachments` (ili `Prilozi`) – zasebna mapa gdje će Obsidian po defaultu spremati različite **datoteke** koje dodamo u bilješke (npr. slike, PDF-ovi i sl.). Provjerite u _Settings → Files & Links → Attachment folder_ da je putanja na ovu mapu, kako biste održali spremište organiziranim, odnosno da svu sve slike na jednom mjestu).

> [!TIP] Važna napomena
> Ovo je samo jedna od mogućih struktura i načina organizacije "proširenog uma". Neki će preferirati minimalizam (sve bilješke u jednom folderu + tagovi za kategorije), drugi će razviti vrlo detaljnu hijerahiju. Za početak, napravite gore navedene mape (desni klik u File Exploreru → New Folder). Time ćete u maniri "arhitekata"označiti glavne zone unutar spremišta. Nadalje, prilikom izrade konkretnih bilješki, razmislite pripada li u neku od ovih mapa. Ako niste sigurni, ubaciti na "hlađenje" u `00 Inbox` pa ćete kasnije odlučiti.

**Konvencije imenovanja:** Bilješke u Obsidianu su obične datoteke pa je dobro usvojiti i konzistentan način imenovanja:
- Kraći **naslovi bilješki** koji jasno opisuje sadržaj (npr. “Teorija kognitivnog opterećenja” umjesto cijelog pitanja).
- Kod literaturnih bilješki u naslov možete staviti npr. prezime autora i godinu: “Novak2021 - Analiza podataka” radi lakšeg pamćenja ili referenciranja.
- Za vođenje dnevnika (eng. *journaling*) i dnevne bilješke, Obsidian koristi **Daily notes** plugin koji kreira bilješke nazvane po datumu (YYYY-MM-DD). To je također koristan način vođenja dnevnika rada. Ovdje savjetujem instalaciju **Calendar** plugina koji vizualno prikazuje kalendar i omogućuje vođenje dnevnih, tjednih, mjesečnih, kvartalnih ili godišnjih bilješki.

**Mapa vs. link vs. tag:** Kratko razjašnjenje – ako se pitate treba li nešto biti mapa ili bilješka ili tag:
- Mape su grube, fizičke podjele i vrlo korisne su za **različite vrste sadržaja** (kao gore Projekti/Resursi itd.). Preporuča se ne stvarati previše duboke hijerarhije mapa za tematske podjele; radije koristite bilješke i tagove za teme. Ne zaboravite, bilješku ili dokument ne možete istovremeno smjestiti u dvije ili više mapi! Možete, ali onda ih duplicirate ili koristite virtualne linkove (eng. *shortcuts*).
- Bilješke možete i koristiti za izradu naređenih *kategorija* ili tzv. **MOC (Map of Content)** – npr. možete imati bilješku “Machine Learning” koja ne sadrži tekst nego popis linkova na sve ostale bilješke, literaturu i podteme vezane za ML. Ovo je često bolja opcija nego mapa jer u MOC bilješku možete dodati kontekst i navesti opis uz svaki link. Zamislite da su MOC zapravo dinimčna verzija *TOC* (kazala sadržaja, a u ovom slučaju kazala bilješki).
- Tagovi su brzi način označavanja teme ili statusa (npr. #ideja, #treba-razraditi, #literatura). Tagovi su globalni, ne moraju se nalaziti u nekoj “nadređenoj” bilješci i možete jednoj bilješci dodati više tagova. Kasnije ih možete filtrirati ili vizualizirati. Tagovi su odlični za povezivanja sadržaja unutar kategorija – npr. tag #članak može ići uz sve bilješke koje su sažeci članaka, bez obzira u kojem su folderu.

Kroz praksu ćemo postupno razviti osjećaj za ono što nam je potrebno – ne brinite ako sada ne možete predvidjeti savršen sustav. Krenite s jednostavnom strukturom i dopustite da se prilagodi vašem stilu bilježenja.
## 7. Povezivanje bilješki: linkovi, reference i graf

Jedna od najvećih snaga Obsidiana je lakoća kojom možete **povezivati bilješke**. Već smo spomenuli sintaksu za unutarnje linkove `[[ ... ]]`. Sada ćemo to isprobati i objasniti povezane značajke.

**Stvaranje linka na postojeću bilješku:** Otvorite neku bilješku koju ste ranije stvorili (ili napravite novu) i upišite `[[`pa počnite pisati naziv druge bilješke (ili dio sadržaja). Vidjet ćete da Obsidian nudi *auto-complet* popisa postojećih naslova dok tipkate. Odaberite željenu bilješku i pritisnite Enter – Obsidian će umetnuti link. U _Preview_ prikazu, taj link je klikabilan i vodi vas na tu bilješku. Ovo je **jednosmjerna veza** stvorena u tekstu _A_ koja vodi na _B_.

**Backlinks (povratne veze):** Ono što Obsidian radi automatski jest da na odredišnoj bilješci _B_ prikazuje (u desnom sidebaru) da je _A_ povezana s njom. Time dobijemo **dvosmjernu povezanost** – bez potrebe da ručno u bilješci B navodimo A. Panel _Backlinks_ prikazuje sve bilješke koje linkaju na trenutnu, što pomaže da vidimo kontekst: npr. ako imate bilješku o nekom teorijskom pojmu, backlinks će pokazati sve literaturne bilješke gdje se pojavio taj pojam, sve projektne bilješke koje ga referenciraju itd. Tijekom građenja sustava, korisno je povremeno provjeriti backlinks na važnijim bilješkama kako biste eventualno dodali povratni link ako ima smisla (iako nije nužno).

**Izrada nove bilješke putem linka:** Ako u nekoj bilješci upišete `[[Novi pojam]]` i zatvorite zagrade, stvorit ćete potencijalnu poveznicu prema novoj bilješci. Klikom na takav link Obsidian će odmah stvoriti novu bilješku pod nazivom “Novi pojam”. Ovo je odličan način “vrtlarenja”: dok pišete jednu bilješku, shvatite da bi neki termin trebao svoju bilješku – samo ga stavite u dvostruke zagrade i nastavite dalje, a kasnije ćete popuniti tu novu bilješku sadržajem. Na taj način gradite mrežu _in situ_.

**Embedanje bilješki:** Još naprednija značajka je da možete uključiti sadržaj jedne bilješke u drugu koristeći sintaksu `![[Naziv bilješke]]`. To ubacuje dinamički prikaz te bilješke. Ovo je korisno za npr. izradu _preglednih bilješki_ koje sakupljaju više izvora.

**Graf prikaz:** Klikom na ikonicu “Open Graph view” u lijevoj vrpci, otvorit će se **globalni graf** svih vaših bilješki. Svaka bilješka je prikazana kao čvorište (točka), a linkovi kao linije između čvorišta. U početku, s malim brojem bilješki, graf neće izgledati spektakularno, ali kako spremište bude raslo, vidjet ćete mrežu bilješki povezanih u klastere i eventualno neke izolirane točke (tzv. _siročad_ – bilješke bez veza). Graf je koristan vizualni alat za **uvid u cjelinu** vašeg znanja – primjerice, možete identificirati teme s puno poveznica (centroidi) i one koje su osamljene (što može značiti da im trebaju još poveznica ili da nisu integrirane u vaš sustav). Obsidian omogućuje filtriranje grafa (po tagu, po dijelu naziva, po stupnju povezanosti, dijeljenim prilozima) i prikaz **lokalnog grafa** za pojedinu bilješku (desni klik na bilješku → Open local graph), gdje vidite samo njene neposredne veze i veze u 1-2 razine udaljenosti. Lokalni graf je odlično pomagalo kad želite sagledati **kontekst** neke bilješke na vizualan način – npr. vidjeti sve druge koncepte povezane s njom. 

> [!NOTE] Ne precjenjujte vrijednost grafa
> Graf ne treba ni precjenjivati – sam po sebi “mreža točkica” neće odraditi magiju povezivanja umjesto vas, ali je dobar **orijentir** i može vas potaknuti da povezujete više (nitko ne voli vidjeti previše "siročadi").

**Reference na literaturu:** Osim internih linkova, u bilješkama ćete često koristimo reference koji upućuju na literaturu. Ne postoji jedinstven standard unutar Obsidiana, ali preporučujemo koristiti **Zotero** za upravljanje formalnim citatima. Na primjer, u tekst bilješke možete zalijepiti (copy&paste iz Zotero) _APA citat_ ili ključ (ako koristite Better BibTex plugin za Zotero koji generira citekey). Alternativno, neki Obsidian korisnici koriste [[Zotero Integration plugin]] koji omogućuje pretragu Zotero bibliografije direktno iz Obsidiana i automatsko umetanje citata ili bibliografskih zapisa. Za početak, možete ručno navesti literaturu na dnu bilješke ili koristiti podnožne bilješke u kombinaciji sa popisom izvora. Ključ je konzistentnost – npr. odredite da sve literaturne bilješke sadrže na dnu sekciju “Literatura” s navedenim punim referencama onoga što je citirano u toj bilješci. To osigurava da i izvan Obsidiana (npr. ako nekome šaljete tu bilješku) reference nisu izgubljene.

Ukratko, **umrežavanje bilješki** srce je PKM-a u Obsidianu. Povezujte obilato, koristite graf za uvide, i ne zaboravite povremeno proći kroz nove bilješke i povezati ih gdje smisleno. Vaš cilj je da s vremenom svaka nova informacija **nađe svoje mjesto** u mreži postojećeg znanja.

## 8. Korištenje spremišta: pretraživanje, filtriranje i izvlačenje (dodane) vrijednosti

S vremenom ćete u svom vaultu imati stotine bilješki. Kako onda **pronaći ono što vam treba**? Obsidian ima nekoliko alata koji olakšavaju korištenje prikupljenog znanja:
- **Brza pretraga (Quick Switcher):** Tipkovni prečac `Ctrl+O` otvara brzu tražilicu bilješki po naslovu. Upisivanjem dijela naslova dobit ćete popis podudarnih bilješki – odlično za brzi prelazak na određenu bilješke (npr. kucajte “notes” i odmah idite na “Note Taking in Markdown” bilješku).
- **Globalna pretraga sadržaja:** U lijevom sidebaru, klikom na _Search_ (povećalo), možete upisati bilo koji pojam i Obsidian će pretražiti **sav tekst unutar bilješki**. Podržava regularne izraze i logičke operatore, ali i jednostavan upit “riječ1 riječ2” koji pronalazi bilješke gdje se pojavljuju obje riječi kao fraza. Rezultati se prikazuju kao popis ulomaka. Ova pretraga je srž korištenja – npr. želite li naći gdje ste spomenuli “Bloomova taksonomija”, ne morate se sjećati gdje, dovoljno je pretražiti pojam.
- **Filtriranje po tagovima:** Ako dosljedno koristite **tagove** (oznake) za ključne kategorije, u tag panelu (lijevi ili desni sidebar, ovisno gdje ih smjestite), klik na određeni tag prikazat će sve bilješke u kojima je zastupljen. Tako možete npr. vidjeti sve bilješke označene s `#literatura` (svi sažeci članaka), `#ideja`(sve vaše vlastite ideje za projekte), `#todo`(ako označavate bilješke koje još treba dovršiti), `#filmovi`, `#serije`, itd.
- **Pregled po datumu:** Ako koristite dnevne bilješke (Daily notes plugin) ili  oznake datuma u bilješkama, onda ih možete kronološki pregledati. Tu pomaže **Calendar plugin** (o kojem slijedi) koji kalendarski vizualizira dnevne bilješke.

**Dataview upiti:** Za naprednije korisnike, _Dataview_ plugin omogućuje upravljanje bilješkama kao **bazom podataka**, odnosno omogućuje **postavljane upita**. Upit možete upisati u bilo koju bilješku, npr. 

```dataview
LIST FROM #literatura AND "02 Područja/Obrazovanje"
```