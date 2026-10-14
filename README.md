# Jednadvacet skills

Vlastní [skills](https://github.com/vercel-labs/skills) pro projekty komunity
Jednadvacet.org. Skill se publikuje do tohoto GitHub repozitáře a do jednotlivých
projektů se přidává přes CLI `npx skills`. Pro použití se můžeš inspirovat v projektu [website](https://github.com/jednadvacetorg/website).

[Otevřít v ChatGPT][chatgpt-work-skills]

<details>
<summary>Ostatní AI nástroje</summary>

Skilly můžeš zkusit v jakémkoliv agentovém AI nástroji. Zkopíruj tento prompt:

```text
Používej skilly z https://github.com/jednadvacetorg/skills.

Zkus je nainstalovat nativním způsobem pro tento nástroj. Pokud to nepůjde, stáhni repozitář do dočasného pracovního adresáře a používej skilly pouze v této konverzaci.

Nejdřív načti jen YAML metadata všech SKILL.md, zejména name a description. Podle každého úkolu vyber relevantní skilly a před použitím přečti jejich úplné instrukce a potřebné reference. Pokud se žádný nehodí, použij běžný postup. Stručně potvrď dostupné skilly a počkej na zadání.

Po dokončení úkolu nebo při zablokování postupu zvaž návrh GitHub issue k významným či opakovaným problémům se skilly. Pokud můžeš, ověř duplicitu. Uveď skill, verzi repozitáře, kroky k reprodukci, očekávané a skutečné chování a nalezené řešení nebo blokaci. Rozliš chybu skillu od omezení prostředí, označ nejisté příčiny a vynech citlivé údaje. Návrh ukaž uživateli; zveřejni ho jen na jeho výslovný pokyn.
```

Umí tvůj nástroj otevřít předvyplněný prompt přes odkaz? Vítáme PR, který sem takový odkaz přidá.

</details>

## `jednadvacet-copywriter`

Skill pro psaní a korektury v češtině pro bitcoinovou komunitu Jednadvacet -
pozvánky na akce, vzdělávací posty, web copy, příspěvky na sociální sítě a e-maily.
Definuje tón, cílovou skupinu, zakázaný slovník (Bitcoin klišé) a strukturu textů
podle typu. Snaží se eliminovat konstrukce, které lidi vnímají jako AI slop.

```bash
npx skills add jednadvacetorg/skills --skill jednadvacet-copywriter
```

Zvaž také přidání instrukcí do svého `AGENTS.md`/`CLAUDE.md`:

```
# Copywriting

- Before writing or editing Czech texts, load the `jednadvacet-copywriter` skill and follow it.
- For best results use Claude Opus model. If you are not Opus, recommend switch to Opus for copywriting job.
```

## `jednadvacet-image-style`

Skill pro přípravu fotografií a obrázků pro Jednadvacet — náhledy článků a podcastů,
portréty, obrázky pro sdílení a YouTube. Popisuje ořez, změnu velikosti, barevné
úpravy, odstranění pozadí i generování a úpravy pomocí AI.

Sjednocuje vizuální styl: přirozené fotografie, grafitové stíny, teplé světlé tóny
a střídmé oranžové akcenty. Hlídá zachování tváří, textů a log i použitelnost jedné
fotografie v různých ořezech s titulkem a logem.

Pro lokální úpravy používá ImageMagick. Součástí je CLI pro obrazové modely přes
PPQ, které vyžaduje Node.js 24+ a API klíč v `PPQ_API_KEY` nebo uložený v OpenCode.
Před úpravou si s tebou agent vybere nástroj; u placených modelů ověří aktuální
možnosti a cenu a počká na schválení rozsahu.

```bash
npx skills add jednadvacetorg/skills --skill jednadvacet-image-style
```

Zvaž také přidání instrukce do svého `AGENTS.md`/`CLAUDE.md`:

```text
# Images

- Before inspecting, editing, preparing or generating photographs or raster image assets, load the `jednadvacet-image-style` skill and follow it.
```

Podrobný postup najdeš v [SKILL.md](skills/jednadvacet-image-style/SKILL.md)
a vizuální pravidla v [průvodci stylem](skills/jednadvacet-image-style/references/style-guide.md).

[chatgpt-work-skills]: https://chatgpt.com/?surface=work&prompt=Pro%20tuto%20konverzaci%20pou%C5%BE%C3%ADvej%20skilly%20z%20https%3A%2F%2Fgithub.com%2Fjednadvacetorg%2Fskills.%0A%0ASt%C3%A1hni%20aktu%C3%A1ln%C3%AD%20v%C3%BDchoz%C3%AD%20v%C4%9Btev%20repozit%C3%A1%C5%99e%20pouze%20do%20do%C4%8Dasn%C3%A9ho%20pracovn%C3%ADho%20adres%C3%A1%C5%99e%20t%C3%A9to%20konverzace.%20Neinstaluj%20skilly%20glob%C3%A1ln%C4%9B%20a%20neukl%C3%A1dej%20je%20do%20m%C3%A9ho%20profilu%20ani%20trval%C3%BDch%20instrukc%C3%AD.%0A%0ANajdi%20v%C5%A1echny%20soubory%20SKILL.md%20v%20repozit%C3%A1%C5%99i.%20Nejd%C5%99%C3%ADv%20na%C4%8Dti%20pouze%20jejich%20YAML%20metadata%2C%20zejm%C3%A9na%20name%20a%20description.%20Uchovej%20si%20p%C5%99ehled%20dostupn%C3%BDch%20skill%C5%AF%20a%20cest%20k%20jejich%20soubor%C5%AFm%20pro%20tuto%20konverzaci.%0A%0AP%C5%99i%20ka%C5%BEd%C3%A9m%20%C3%BAkolu%20podle%20metadat%20vyber%20relevantn%C3%AD%20skill%20nebo%20v%C3%ADce%20skill%C5%AF.%20P%C5%99ed%20jejich%20pou%C5%BEit%C3%ADm%20p%C5%99e%C4%8Dti%20cel%C3%BD%20p%C5%99%C3%ADslu%C5%A1n%C3%BD%20SKILL.md%20a%20podle%20pot%C5%99eby%20jeho%20odkazovan%C3%A9%20reference.%20%C5%98i%C4%8F%20se%20jejich%20instrukcemi.%20%C3%9Apln%C3%A9%20instrukce%20ostatn%C3%ADch%20skill%C5%AF%20p%C5%99edem%20nena%C4%8D%C3%ADtej.%20Pokud%20se%20%C5%BE%C3%A1dn%C3%BD%20skill%20nehod%C3%AD%2C%20vy%C5%99e%C5%A1%20%C3%BAkol%20b%C4%9B%C5%BEn%C3%BDm%20postupem.%0A%0ADostupnost%20n%C3%A1stroj%C5%AF%20a%20p%C5%99%C3%ADpadn%C3%A9%20p%C5%99%C3%ADstupy%20%C5%99e%C5%A1%20a%C5%BE%20u%20konkr%C3%A9tn%C3%ADho%20%C3%BAkolu.%20Po%20na%C4%8Dten%C3%AD%20metadat%20stru%C4%8Dn%C4%9B%20potvr%C4%8F%20dostupn%C3%A9%20skilly.%20Pokud%20n%C4%9Bco%20nelze%20na%C4%8D%C3%ADst%2C%20%C5%99ekni%20p%C5%99esn%C4%9B%20co.%20Pak%20po%C4%8Dkej%20na%20moje%20zad%C3%A1n%C3%AD.%0A%0ANa%20konci%20%C3%BAkolu%2C%20po%20jeho%20dokon%C4%8Den%C3%AD%20nebo%20p%C5%99i%20zablokov%C3%A1n%C3%AD%20dal%C5%A1%C3%ADho%20postupu%2C%20zhodno%C5%A5%2C%20zda%20se%20u%C5%BEivatel%20nebo%20agent%20pot%C3%BDkal%20s%20v%C3%BDznamn%C3%BDmi%20%C4%8Di%20opakovan%C3%BDmi%20obt%C3%AD%C5%BEemi%20souvisej%C3%ADc%C3%ADmi%20s%20t%C4%9Bmito%20skilly.%0A%0APokud%20by%20popis%20probl%C3%A9mu%20mohl%20pomoci%20skilly%20zlep%C5%A1it%2C%20zva%C5%BE%20n%C3%A1vrh%20GitHub%20issue%20v%20tomto%20repozit%C3%A1%C5%99i.%20Rozli%C5%A1%20probl%C3%A9m%20ve%20skillu%20od%20omezen%C3%AD%20prost%C5%99ed%C3%AD%2C%20chyb%C4%9Bj%C3%ADc%C3%ADho%20p%C5%99%C3%ADstupu%20nebo%20jednor%C3%A1zov%C3%A9%20chyby.%20Pokud%20m%C3%A1%C5%A1%20p%C5%99%C3%ADstup%20k%20existuj%C3%ADc%C3%ADm%20issues%2C%20ov%C4%9B%C5%99%20p%C5%99%C3%ADpadnou%20duplicitu.%0A%0ANavrhni%20stru%C4%8Dn%C3%BD%20n%C3%A1zev%20a%20popis%20obsahuj%C3%ADc%C3%AD%20pou%C5%BEit%C3%BD%20skill%20a%20verzi%20repozit%C3%A1%C5%99e%2C%20situaci%20a%20kroky%20k%20reprodukci%2C%20o%C4%8Dek%C3%A1van%C3%A9%20a%20skute%C4%8Dn%C3%A9%20chov%C3%A1n%C3%AD%20a%20nalezen%C3%A9%20%C5%99e%C5%A1en%C3%AD%20nebo%20bod%2C%20na%20kter%C3%A9m%20postup%20uv%C3%ADzl.%20Jasn%C4%9B%20ozna%C4%8D%20nejist%C3%A9%20p%C5%99%C3%AD%C4%8Diny%20a%20vynech%20citliv%C3%A9%20%C3%BAdaje.%0A%0AN%C3%A1vrh%20mi%20uka%C5%BE%20a%C5%BE%20po%20v%C3%BDsledku%20%C3%BAkolu%20nebo%20vysv%C4%9Btlen%C3%AD%20blokace.%20Issue%20zve%C5%99ejni%20pouze%20na%20m%C5%AFj%20v%C3%BDslovn%C3%BD%20pokyn.
