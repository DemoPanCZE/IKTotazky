![[01 Historie výpočetní techniky#John Von Neumann]]

# Díly počítače

## Základní deska
- propojuje všechny součásti
	- integrované (zvuková karta, síťová karta)
	- připojuje i napájí (RAM, CPU, M.2 disky)
	- pouze připojuje, napájeny jsou zdrojem (GPU)
	- 
### Porty

#### Audio
- **Základní výstupy**
	- <mark style="background: #BBFABBA6;">Line out</mark> - stereo, front speaker/sluchátka
	- <mark style="background: #ABF7F7A6;">Line in</mark> - obecný audio vstup
	- <mark style="background: #FF5582A6;">Mic in</mark> - vstup pro mikrofon
- **Surround-sound výstupy:**
	- <mark style="background: #FFB86CA6;">CS-Out</mark> - center/subwoofer
	- <mark style="background: #D2B3FFA6;">RS-Out</mark> - rear speakers (černý)
	- <mark style="background: #CACFD9A6;">SS-Out</mark> - side speakers
- Digitální optický audio [[opticalAudio.bmp|port]] - domácí kina, soundbary

#### Video
- **Analogové**
	- VGA (D-sub)
- **Digitální**
	- DVI - digitální i analogový spoj
	- HDMI - přenos obrazu i zvuku, různé velikosti
	- DisplayPort

#### Síťové
- ethernet port - konektor **RJ-45**


### Chipset
- sada integrovaných obvodů starající se o komunikaci mezi CPU, pamětí a I/O zařízeními
- typicky dva obvody - **Northbridge** a **Southbridge**, nově však bývají i v jednom čipu
- [[intelChipset.bmp|schéma (obrázek)]]
#### Northbridge
- *"systémový řadič (memory controller hub)"*
- komunikace mezi CPU, RAM a PCI-Express sběrnicí (dříve AGP portem)
- spojení se southbridgem

#### Southbridge
- *"vstupně-výstupní řadič (I/O Controller Hub)"*
- není přímo spojen s CPU
- pomalejší funkce
- připojení:
	- PCI sloty
	- SATA
	- USB
	- Ethernet
	- Audio Codec
	- CMOS paměť (nastavení biosu, napájí [[cmosBattery.bmp|CMOS baterie]])
	- Super I/O - čip s rozhraními pro low-speed zařízení:
		- obsluha disketové mechaniky
		- paralelní port (pro tiskárnu)
		- sériový port RS-232
		- PS/2 porty [[superIOporty.bmp|(Obrázek portů)]]
		- monitoring teplot
		- ovládání větráků

## CPU
- zpracovává instrukce programů ze strojového kódu (*machine code*)
- složený z miliard tranzistorů
- největšími výrobci jsou **Intel** a **AMD** a nově **Apple**
- na mobilním trhu **Qualcomn** (čipy Snapdragon), **Samsung** (Exynos) nebo **Apple M** čipy

### Parametry:
#### Frekvence
- počet instrukcí za sekundu
- vychází z ipc (instructions per cycle)
- v řádu gigahertzů
#### Počet jader
- každé jádro je mikroprocesor
- více jader je užitečné pro zátěž, kterou lze rozdělit, např. renderování
#### Socket
- konektor pro zapojení do motherboardy
- cpu a mb musí mít kompatibilní socket

### Chlazení
- klasický chladič - pasivní heatsink a větrák
- vodní chlazení: radiator s větráky, reservoir, pumpa, water blocks, které chladí komponenty

## RAM
- pracovní prostor pro CPU
- slouží pro dočasné ukládání dat běžících procesů

### Parametry:
#### Kapacita
- v řádech jednotek GB
#### Frekvence
- v MHz (= 2x megatransfery/s) (current gen DDR4 - 3200MHz)
#### Typ
- DDR3, DDR4, DDR5

## Pevný disk
- trvalé ukládání dat
### Typy
- **HDD** - magnetický princip: otáčející se plotny, čtecí/zapisovací hlava
- **SSD** - čistě elektronický, flash paměť, rychlejší a odolnější (otřesy), dražší (dnes ne o moc)
- **M.2 SSD** - menší rozměr

### Parametry:
#### Kapacita
- dnes už v řádech jednotek TB
#### Velikost
- 3,5" HDD, 2,5" SSD nebo HDD do notebooků
- M.2 jsou menší, (22mm x 80mm)

## Zdroj (PSU)
- převádí 230V AC na menší DC
- *funfact*: kabely jsou color-coded podle napětí

### Parametry:
#### Výkon
- kolik energie je schopen dodat /s
- kancelářské do 350W, herní 500W - 750W
- Rule of thumb - 2x draw GPU+CPU + 40W pro zbytek
#### Účinnost
- kvalitní zdroj alespoň 80 % 
#### Velikost, výbava
- modulární (= odpojitelné kabely)
- regulace otáček
- display zobrazující power draw

## Skříň

### Parametry
#### Velikost
- mini tower
- mid tower
- full tower
#### Formát MB
- ATX
- Micro-ATX
- Mini-ATX

## Grafická karta a GPU
- koprocesor, ve specifických výpočtech rychlejší než CPU
- může být integrovaná, pak místo vlastní paměti používá RAM
- vytváří grafický výstup:
	- vytváří obraz
	- dekóduje video *(?)*
	- zpracovává 3D geometrii na 2D obraz

## Zvuková karta
- většinou integrovaná na motherboardě
- umožňuje vstup, výstup a zpracování zvuku (DAC, ADC převodníky)
- externí zvukové karty používány pro profesionální účely (nahrávání), nejčastěji přes USB/FireWire

## Síťová karta
- komunikace a přenos dat mezi pc, připojení k síti
- většinou integrovaná na motherboardě

## Optická mechanika
- čte a zapisuje na optické disky - CD, DVD