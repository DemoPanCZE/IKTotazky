# Číselná soustava
- způsob reprezentace čísel
- dělí se na poziční a nepoziční

# Nepoziční soustavy
- hodnota číslice není dána jejím umístěním
- zastaralé, dnes se téměř nepoužívají
- často neobsahovaly nulu a záporná čísla, zápis byl dlouhý
- např. římské číslice, egyptské číslice, řecké číslice (zápis pomocí písmen alfabety)

## Římské číslice
- vznikly přirozeně, podle vizuálních hodnot
	- **I**, **V**, a **X** vychází z prstů a dlaní
	- **C** (centum) a **M** (mille) z latiny, **L** a **D** grafickým "rozpůlením" znaků **C** a **M** (ale moc to tam nevidim)
- mnemotechnická pomůcka - ***I**van **V**edl **X**énii **L**esní **C**estou **D**o **M**ěsta*
- nebo Martinákova pomůcka - ***I**van **V**zal **X**énii **LCD** **M**onitor*
| Římské číslo | Arabské číslo |
| ------------ | ------------- |
| I            | 1             |
| V            | 5             |
| X            | 10            |
| L            | 50            |
| C            | 100           |
| D            | 500           |
| M            | 1 000         |


# Poziční soustavy
- charakterizovány tzv. základem neboli bází (anglicky radix, značí se **r**)
	- = kladné celé číslo definující maximální počet číslic, které jsou v dané soustavě k dispozici
- každé číslo v poziční soustavě může mít celočíselnou a zlomkovou část, ta se odděluje desetinnou čárkou (nebo tečkou)

- **dvojková (BIN)** — binární, _r=2_ 
	- přímá implementace v digitálních elektronických obvodech (použitím logických členů), čili interně ji používají všechny moderní počítače
- **osmičková (OCT)** — oktální, oktalová, _r=8_
- **desítková** **(DEC)** — decimální, dekadická, _r=10_
- **dvanáctková** _— r=12_
	- dnes málo používaná, ale dodnes z ní zbyly názvy prvních dvou řádů – tucet a veletucet
- **šestnáctková (HEX) —** hexadecimální, _r=16_
	- používá se v oblasti informatiky, pro číslice 10 až 15 se používají písmena A až F
- **šedesátková** — sexagesimální, _r=60_
	- používá se k měření času pro zlomky hodiny; číslice se obvykle zapisují desítkovou soustavou jako 00 až 59 a řády se oddělují dvojtečkou

## Binární soustava
- používá 0 a 1
- jednoduše implementovatelná v elektrickém obvodu - vypnuto × zapnuto
- logické operace - true × false
### Převod

#### bin –> dec
**111001**<sub>2</sub> = 1⋅2<sup>5</sup> + 1⋅2<sup>4</sup> + 1⋅2<sup>3</sup> + 0⋅2<sup>2</sup> + 0⋅2<sup>1</sup> + 1⋅2<sup>0</sup> = **57**<sub>10</sub>
| 1             | 1             | 1             | 0             | 0             | 1             |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |

#### dec –> bin
- převod opakovaným dělením dvěma a zápisem zbytku
**356<sub>10</sub> = 101100100<sub>2</sub>
| ÷2  | **výsledek** | **zbytek** |
| --- | ------------ | ---------- |
| 356 | 178          | 0          |
| 178 | 89           | 0          |
| 89  | 44           | 1          |
| 44  | 22           | 0          |
| 22  | 11           | 0          |
| 11  | 5            | 1          |
| 5   | 2            | 1          |
| 2   | 1            | 0          |
| 1   | 0            | 1          |

### Operace

#### Sčítání
- ***Pravidla***
	- 0 + 0 = 0
	- 0 + 1 = 1
	- 1 + 0 = 1
	- 1 + 1 = 10
- ***Příklady*
	- 10001 + 11101 = 101110
	- 1011001 + 111010 = 10010011

#### Odčítání
- ***Pravidla***
	- 0 – 0 = 0
	- 0 – 1 = 1 (půjčí se 1 zleva)
	- 1 – 0 = 1
	- 1 – 1 = 0
- ***Příklady*
	- 1011011 − 10010 = 1001001
	- 101101 − 100111 = 110

#### Násobení
- ***Pravidla***
	- 0 × N = 0
	- 1 × 1 = 1
	- klasické násobení pod sebou, násobím členy druhého čitatele a posouvám, pak sečtu
- ***Příklady*
	- 1101 * 1010 = 10000010


## Hexadecimální soustava
- mocniny šestnácti
- hodnoty 0-15
- číslice pro 0-9, písmena A-F pro 10-15
- využíváná např. při **zápisu barev**
	- pomocí dvou hex znaků lze zapsat 256 hodnot (0-255)
	- barevný hex kód má 6 znaků, 2 pro každou barvu v RGB (RR GG BB)
	- \#B611AE = (R:182 G:17 B:174)
### Převod
#### hex –> dec
**B6**<sub>16</sub> = 176 + 6 = **182**<sub>10</sub>
| B (=11)             | 6                  |
| ------------------- | ------------------ |
| 11 × 16<sup>1</sup> | 6 × 16<sup>0</sup> |
| 176                    |   6                 |


# Kódování
- =konverze dat do specifikovaného formátu

## Text
- tzv. **znakové sady** - každý znak má přiřazeno určité číslo
- **ASCII** (*American Standard Code for Information Interchange*)
	- nejstarší znaková sada
	- 7 bitů (128 hodnot)
	- každý znak zabírá právě 1 byte
	- velká a malá písmena anglické abecedy, číslice, základní symboly
	- 33 řídících a 95 tisknutelných znaků
	- později vznikaly 8-bitové sady pro různé jazyky
- **Kód bratří Kamenických**
	- 8-bitová sada pro češtinu a slovenštinu, vyvinutá pro MS DOS
- **Windows-1250**
	- 8-bitová sada pro východoevropské jazyky

### Unicode 
- = norma pro zpracování většiny písem v současnosti na Zemi
- přes 140 000 znaků, [159 písem](https://unicode.org/charts/), sady symbolů
- maximální velikost je 1,114,112 kódových bodů (0<sub>16</sub> - 10FFFF<sub>16</sub>) = (0<sub>10</sub> - 1,114,111<sub>10</sub>)
- místo *znaků* používán pojem *grafém*
- každý má přiřazen kódový bod (hodnotu), např. 👍 U+1F44D<sub>16</sub> = 128077<sub>10</sub>
- U+ značí začátek codepointu
- Nejpoužívanější sady; názvy podle min. počtu bitů pro znak
	- **UTF-8** - nejrozšířenější, angličtina má nejkratší stringy(=> zpětná kompatibilita s ASCII), znaky nemusí mít stejný počet bitů
	- **UTF-16**
	- **UTF-32**

## Obraz

### Bitmapová grafika
- obraz je uložen jako mřížka pixelů
- každý pixel má polohu a barvu podle modelu (RGB, CMYK...)
- barevná hloubka (bit depth) = počet barev, které může mít pixel (nebo color channel)
- **[[bitdepth.bmp|Bit depth 2 × 4 × 256 (obrázek)]]**
- JPEG je '8-bitový' formát, u barevného obrázku je ale hloubka každého pixelu 24 bitů (8b pro R,G a B)
- 8-bit RGB má 256<sup>3</sup> možných barev
- vyšší bit depth používán např. v RAW formátu fotografií (12-bit, 14-bit)
- **editory:** Adobe Photoshop, GIMP, mspaint, Photopea (český, JS webová aplikace)
- **formáty:** .jpg, .png, .gif, .tiff, .psd, .xcf (gimp)
- #### Pros
- přiblížení realitě (fotografie)
- jde snadno editovat
- #### Cons
	- ztráta kvality při změně velikosti
	- chybí možnost editace částí obrazu
	- úprava není nedestruktivní (mimo editory s vrstvami, maskami...)
	- velké soubory při editaci

### Vektorová grafika
- základem je analytická geometrie
- obraz se skládá z [[bezierCurve.bmp|Bézierových křivek]] spojujících kotevní body
	- **Bézierova křivka** - Pierre Bézier, čtyřmi body lze popsat jakýkoli úsek křivky
- křivky mají výplň barvou nebo gradientem
- používá se pro sazbu, ilustrace, diagramy, loga
- **editory:** Adobe Illustrator, Inkscape, CorelDRAW
- **formáty:** .ai, .pdf, .svg (*scalable vector graphics*)
- #### Pros
	- obrázky lze zvětšovat bez ztráty kvality
	- skládají se z objektů, se kterými lze pracovat odděleně
	- menší velikost proti rastrovým obrázkům
- #### Cons
	- nehodí se pro zápis složitých barevných ploch
	- u složitějších obrázků náročnější na paměť a cpu

## Zvuk
- zvuk je pomocí mikrofonu převeden na analogový elektrický signál
- **vzorkování** (sampling) - vybírání hladin intenzity signálu v určitých časových bodech
	- *sample rate* - čím [[sampleRate.webp|více vzorků]], tím kvalitnější zvuk
	- standardní jsou 44,1kHz a 48kHz (CD quality)
- **kvantování** - zaokrouhlení skutečných hodnot (analogový signál jich má nekonečno)
- výsledkem **vzorkování** a **kvantování** je konečný počet vzorků s konečným počtem jejich hodnot
- **formáty:** mp3, aac, FLAC, Apple Lossless (bezeztrátové)

## Video
- [ ] video: zvuk a video, video = rychle obrazky, setrvacnost a nedokonalost oka, framerate