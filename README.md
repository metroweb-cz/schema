Schéma sítě pražského metra
===========================
Toto schéma má reprezentovat kolejovou síť pražského metra k datu platnosti. Odvozené historické mapy nemusí odrážet skutečný stav rozložení kolejí v dané době. 

Schéma je navrženo tak, aby se jeho vzhled dal snadno upravovat pomocí CSS a manipulovat pomcí Javascriptu. Základní grafická podoba byla vytvořena pomocí Autocadu a upravena v Inkscape.

Soubory
-------
- `[mapa.html](mapa.html)`: Hlavní soubor určený pro prohlížení na webu
- `mapa1.css`: Základní (tříbarevný) stylopis
- `mapa2.css`: Stylopis s barevným rozdělením provozních úseků
- `mapa4.css`: Stylopis s animací průběhu otevírání provozních úseků
- `[mapa1.pdf](mapa1.pdf)` `[mapa2.pdf](mapa2.pdf)`: Schemata ve formátu PDF pro tisk na papíry řady »A«
- `jquery.min.js`: JQuery pro správnou funkci prvků interakce
- `[mapa.svg](mapa.svg)`: Soubor určený pro editaci ve vektorovém editoru nebo samostatné prohlížení, není interaktivní

Instalace
---------
Všechny výše uvedené soubory (mimo `mapa.svg`) umístěte do jedné složky.

### CSS třídy použité v mapě
- Vše související s tratěmi: `.a` `.b` `.c`
- Vše související se stanicemi `.an` `.bd` `.bo` `.ce` `.ch` `.cm` `.de` `.fl` `.fr` `.frb` `.frc` `.ha` `.hl` `.hn` `.ho` `.hr` `.hu` `.ji` `.jn` `.muc` `.na` `.nb` `.nh` `.nm` `.nr` `.nv` `.op` `.pa` `.pe` `.pn` `.pp` `.pr` `.rd` `.ro` `.rz` `.sd` `.sk` `.sn` `.sr` `.st` `.sz` `.vl` `.vs` `.vy` `.ze` `.zl`
- Provozní úseky: `.ia` `.ib` `.ic` `.ic7` `.iia` `.iib` `.iic` `.iiib` `.iiic` `.va` `.vb` `.ivb` `.ivc1` `.ivc2`
- 1\. a 2. kolej SR-DH: `.sh1` `.sh2`
- Koleje v depu Hostivař do stanice HO `.sh_ho`
- Vše v obvodu depa: `.depo`
- Jednotlivá depa (OZM se bere jako depo a každá ze tří etap stavby depa Zličín má vlastní třídu): `.dh` `.ozm` `.dk` `.depo_zlicin_1` `.depo_zlicin_2` `.depo_zlicin_3` `.depo_nezavisle_trakce_zlicin_1` `.depo_nezavisle_trakce_zlicin_2`
- Obratové koleje: `.obratiste`
- Objekty, které oddělují mimoúrovňové křížení tratí (musí mít barvu pozadí): `.oddelovac`
- Zkratka názvu stanice: `.zkratka`
- Zkušební tratě (ZT depa Hostivař nemá vlastní třídu, použijte identifikátory): `.zkusebni_trat_b` `.zkusebni_trat_c`
- Popisky hlavních kolejí 1 a 2, popisky ostatních kolejí, čárky spojující rámečky popisků s kolejemi: `.popkv` `.popkm ` `.popkc`
- Zarážedla, symboly nástupišť a názvy stanic, kolejové spojky: `.zarazedlo` `.stanice` `.spojka`
- Tabulka s daty: `.tabulka`
- Koleje v provozu s cestujícími a zarážedla, která nejsou v depech: `.trat`
- Symboly mostů a portálů: `.most` `.portal`
- Trať depa, jejíž část se nachází v podzemí: `.podzemi`
- Koleje, které nejsou elektrifikované `.bezproudu`
- Koleje v depech mimo ZT a koleje s provozem s cestujícími: `.kolej`
- Symboly v tabulce s daty o provozních úsecích `.ikonky`
- Hala depa: `.hala`
- Hlavní kolej do depa (pro tvorbu zjednodušených schémat, kde není žádoucí vykreslovat všechny koleje: `.hlavni`
- Velké písmeno trasy: `.pismeno_trasy`

### Identifikátory (pro jednotlivé objekty):
- Celý obrázek `#schema`
- Nástupiště stanic; stanice s postranním nástupištěm mají připojeno číslo
 koleje `_1k` nebo `_2k`. `#vy_1k` nebo `#vy_2k` `#an` `#bd` `#bo` `#ce` `#ch` `#cm` `#de` `#fl` `#ha` `#hl` `#hn` `#ho` `#hr` `#hu` `#in` `#ip` `#ji` `#jp` `#kb` `#kc` `#kl` `#kn` `#kr` `#la` `#lk` `#lt` `#lz` `#ma` `#mo` `#na` `#nb` `#nh` `#nm` `#nr` `#nv` `#op` `#pa` `#pe` `#pn` `#pp` `#pr` `#rd` `#ro` `#rz` `#sd` `#sk` `#sn` `#sr` `#st` `#sz` `#vl` `#vs` `#vy` `#ze` `#zl`
- Zkušební tratě: `#zt_a` `#zt_b` `#zt_c`
- Haly dep: `#depo_hostivar` `#depo_kacerov` `#depo_zlicin_1` `#depo_zlicin_2` `#depo_zlicin_3` `#depo_nezavisle_trakce_hostivar` `#depo_nezavisle_trakce_kacerov` `#depo_nezavisle_trakce_zlicin_1` `#depo_nezavisle_trakce_zlicin_2` `#ozm`
- Mosty: `#most_chlumecka` `#most_depo_hostivar` `#most_krc` `#most_prokopske_udoli` `#most_vysehrad`
- Objekty, které oddělují mimoúrovňové křížení tratí (musí mít barvu pozadí): `#oddelovacx`, kde x je číslo 1-10
- Identifikátory barevných přechodů použitých v přestupních stanicích: `#prechod_fr` `#prechod_ms` `#prechod_mu`
- Nadpis mapy a text v pravém dolním rohu: `#titulek` `#tiraz`
- Ikonka s licencí: `#licence`
- Vltava: `#vltava`
- Pozadí celé mapy: `#pozadi`
- Každý nakreslený objekt má přidělené ID, podle kterého ho lze dohledat

### Třídy a identifikátory ovládacího panelu v souboru mapa.html
- `.bold` – Písmo nadpisů v rámečku
- `.mapa1` `.mapa2` – Vyskytuje se v přepínači stylů. Určí, na který pdf soubor bude odkaz směřovat. Proto je nutné, aby se název třídy shodoval s názvem souboru, na který odkazuje.
- `.odrazka` – Odrážka v seznamu, pro vložení obrázku
- `.pdf` - Ikonka pdf souboru
- `.radio` – rámeček s přepínači radio
- `.zmensi` `.zvetsi` – Ikonky
- `#chck1` `#chck2` `#chck3` – Zaškrtávátka
- `#nastaveni` – Rámeček s nastavením
- `#pdf` – Odkaz na pdf soubor
- `#lupa` – Přepínač velikosti
