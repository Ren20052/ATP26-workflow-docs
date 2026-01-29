---
author: Matea Turalija, Dejan Ljubobratović
---

# Suradnički uređivač teksta HackMD i jezik Markdown

[Markdown](https://daringfireball.net/projects/markdown/) je jednostavan jezik za pisanje oblikovanog teksta korištenjem čistog teksta. Njegova osnova karakteristika je jednostavnost i lakoća upotrebe, čineći ga time popularnim alatom za oblikovanje i uređivanje teksta bez potrebe za naprednim tehničkim vještinama. Najčešće se koristi za [pisanje znanstvenih članaka](https://jaantollander.com/post/scientific-writing-with-markdown/), README datoteka i objava na forumima. Više detalja o Markdownu moguće je pronaći na [Wikipedijinoj stranici Markdown](https://en.wikipedia.org/wiki/Markdown).

Datoteke napisane u Markdownu obično koriste ekstenzije kao što su `.md` ili `.markdown`. Na primjer, `primjer.md` je naziv tipične datoteke sa sadržajem u obliku Markdown.

## Uređivači Markdowna

Offline:

- [Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown)
- [Zettlr](https://www.zettlr.com/)
- [ghostwriter](https://ghostwriter.kde.org/)
- [MarkText](https://www.marktext.cc/)
- [RStudio](https://posit.co/download/rstudio-desktop/) ([R Markdown](https://rmarkdown.rstudio.com/) kombinira jezike [R](https://www.r-project.org/) i Markdown)

Online:

- [HackMD](https://hackmd.io/)
- [Visual Studio Code](https://vscode.dev/)
- [Google Colab](https://colab.google/)
- [Jupyter notebooks](https://jupyter.org/)
- [StackEdit](https://stackedit.io/)
- [Dilinger](https://dillinger.io/)
- [Typora](https://typora.io/)
- [Editor.md](https://pandao.github.io/editor.md/en.html)

## Mrežni uređivač Markdowna HackMD

### Kreiranje računa i prijava

Posjetite web stranicu [hackmd.io](https://hackmd.io/) i registrirate se putem ekrana za registraciju. Unesite svoju željenu e-mail adresu i slijedite upute za kreiranje novog korisničkog računa.

Možete koristiti i druge servise za prijavu poput Google ili GitHub računa.

### Moj radni prostor

Kada se prijavite nalazit ćete se u vlastitom radnom prostoru (engl. *My workspace*). Po potrebi možete stvarati odvojene timske radne prostore odabirom *Create new team*.

Novu bilješku možete kreirati klikom na zelenu ikonicu *New note*.

[Sučelje HackMD](https://hackmd.io/c/tutorials/%2Fs%2Ftutorials)-a sastoji se od više ekrana, koji služe za:

- uređivanje,
- pregled,
- podjelu ekrana,
- kreiranje osobne bilješke,
- pomoć,
- pretragu bilješki,
- dijeljenje...

### Uređivanje teksta

#### Naslovi

Naslove označavamo na način da ispred teksta stavimo oznaku `#`. Jedan znak `#` ispred naslova je glavni naslov, dva znaka `##` je naslov druge razine i tako dalje.

!!! admonition "Zadatak"
    - Napišite naslov `Suradnički uređivač teksta HackMD i jezik Markdown` s podnaslovom `Moje bilješke s vježbi`.
    - Isprobavanjem otkrijte koliko razina poglavlja podržava jezik Markdown.

#### Podebljano, kurziv i precrtano

Jednostavno oblikovanje teksta poput korištenja kurziva, podebljanih ili precrtanih riječi pomaže istaknuti važne koncepte unutar dokumenta i učiniti ga čitljivijim.

Podebljana slova (engl. *bold*) u tekstu označavaju se dvjema zvjezdicama `**` prije i nakon riječi. Neki uređivači Markdowna uz zvjezdicu podržavaju i korištenje donjih crta `_` i `__` (engl. *underscore*).

Ukošena slova (engl. *italic*) u tekstu označavaju se jednom zvjezdicom `*` prije i nakon riječi.

Istovremeno podebljana i ukošena slova možemo dobiti korištenjem triju zvjezdica `***` ili kombinacijom s donjim crtama `**_`, `__*`.

Precrtana slova (eng. *strikethrough*) u tekstu označavaju se s dvije tilde `~~` (++alt-graph+1++) prije i nakon teksta.

!!! admonition "Zadatak"
    Napišite sljedeću rečenicu:

    > Ovo je primjer gdje ću koristiti **podebljana**, *ukošena*, ***istovremeno podebljana i ukošena*** te ~~precrtana~~ slova.

#### Komentar

Ukoliko želimo u dokumentu imati komentar koji se neće prikazivati u oblikovanom tekstu, koristimo sljedeću sintaksu:

`<!-- komentar -->`

``` markdown
<!--
Ovaj tekst se
neće vidjetu u izlazu,
to je moj komentar.
-->
```

#### Boja slova

Za promjenu boje slova koristimo [HTML](https://en.wikipedia.org/wiki/HTML) tag `font color` na primjer: `<font color="yellow"> Žuti tekst </font>`.

#### Citiranje

Citat se piše tako da se na početak retka stavi znak `>`.

!!! admonition "Zadatak"
    Napišite sljedeći citat:

    > Ja ne mogu nikoga ništa naučiti, ja ih samo mogu natjerati da misle.

    -- Sokrat

#### Numerirane i nenumerirane liste

Numeriranu listu dobijemo stavljajući redne brojeve prije svakog retka:

``` markdown
Za napraviti:

1. zaliti cvijeće,
2. nahraniti psa,
3. prošetati se.
```

Nenumeriranu listu dobijemo stavljajući znakove `-` ili `*` prije svakog retka:

``` markdown
Moram kupiti:

- kruh,
- mlijeko,
- novine.
```

Potvrdni okvir (engl. *checkbox*) dobijemo stavljajući znak `- [ ]`, odnosno `- [x]` prije svakog retka:

``` markdown
- [ ] za neoznačeni potvrdni okvir
- [x] za označeni potvrdni okvir
```

!!! admonition "Zadatak"
    Napravite sljedeću listu:

    * jezik Markdown
        * jednostavan jezik za pisanje teksta
    * najpoznatiji uređivači jezika Markdown
        1.  Visual Studio Code
            * popularno razvojno okruženje
        2.  HackMD
            * online uređivač
        3. Zettlr
            * offline uređivač

#### Linkovi

Za umetanje linka koristi se sljedeća sintaksa:`[Naziv linka](http://gaseri.org)`.

Ukoliko ne želimo koristiti posebni tekst kao link onda je dovoljno unijeti adresu web stranice unutar znakova `<` i `>`, a Markdown će automatski kreirati link: `<http://gaseri.org>`.

#### Umetanje slika

Za umetanje slike s računala dovoljno kliknuti na *Insert image* ikonicu na alatnoj traci. Takvo ubacivanje slike u nekim markdown uređivačima napravit će gomilu ružnog koda. Zato se preporučuje korištenje online slika.

Za umetanje online slika, dovoljno je u zagradu staviti link na sliku: `![Naziv slike](https://group.miletic.net/images/gaseri-logo-animated.webp)`.

