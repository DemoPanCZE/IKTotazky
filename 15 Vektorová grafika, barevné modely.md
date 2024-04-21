![[02 Číselné soustavy, kódování#Vektorová grafika]]

## Barevné modely
- matematické modly popisující barvy na základě podílu jednotlivých složek

### RGB
- nejrozšířenější - ve fotografii, internetové grafice...
- používaný v barevných monitorech a projektorech - míchání vyzařovaného světla
	- na dislpeji se každý pixel skládá ze tří částí [[ledPixelCloseup.bmp|(obrázek)]]
- aditivní způsob míchání barev, po smíchání všech vzniká bílá
- barva je určena *mohutností* tří základních barev - komponent RGB
- mohutnost komponent se uvádí v procentech nebo 0-255 (v 24-bitové barevné hloubce)
- existuje také RGBA, kdy A je alpha kanál (průhlednost)

### CMYK
- subtraktivní způsob míchání barev, po smíchání všech vzniká černá
- používá se převážně při tisku nebo jiných metod, kdy vznikají barvy mícháním pigmentů
- černá je součástí modelu proto, že v praxi nevzniká černá, ale hnědo-šedivá, je výhodnější tisknout černou zvlášť, než používat všechny tři pigmenty

### HSV
- nejbližší lidskému vnímání světla
- hue, saturation, value
- **Hue** - odstín, převládající barva, poloha na barevném kole
- **Saturation** - sytost, vzdálenost od středu k okrajům
- **Value** - hodnota jasu; vyjadřuje, kolik světla barva odráží
![[hsvValec.png]]