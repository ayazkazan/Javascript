## JavaScript charCodeAt() Metodu ve Örnekleri

`charCodeAt()` metodu, bir JavaScript string ifadesindeki belirli bir indeks numarasındaki karakterin **Unicode (UTF-16)** değerini döndürür. 

**Sözdizimi:**

```javascript
string.charCodeAt(index)
```

* **string:** Unicode değerini almak istediğiniz string ifade.
* **index:** Karakterin string içindeki konumunu belirten 0 tabanlı indeks numarası. 

**Örnek 1: İlk karakterin Unicode değerini alma**

```javascript
const string = "Merhaba Dünya!";
const unicodeDegeri = string.charCodeAt(0);

console.log(unicodeDegeri); // 77 (M harfinin Unicode değeri)
```

Bu örnekte, `charCodeAt(0)` ile "Merhaba Dünya!" string ifadesinin ilk karakteri olan "M" harfinin Unicode değerini (77) alıyoruz ve `unicodeDegeri` değişkenine atıyoruz.

**Örnek 2: İndeks numarası belirtilmezse**

```javascript
const string = "Merhaba Dünya!";
const unicodeDegeri = string.charCodeAt();

console.log(unicodeDegeri); // NaN (İndeks belirtilmediği için)
```

Eğer `charCodeAt()` metoduna bir indeks numarası verilmezse, sonuç `NaN` (Not a Number) olacaktır. 

**Örnek 3: String ifadesini döngü ile karakterlerine ayırma**

```javascript
const string = "JavaScript";

for (let i = 0; i < string.length; i++) {
  const unicodeDegeri = string.charCodeAt(i);
  console.log(`"${string[i]}" karakterinin Unicode değeri: ${unicodeDegeri}`);
}
```

Bu örnekte, `for` döngüsü kullanarak "JavaScript" string ifadesinin her bir karakterini dolaşıyoruz ve `charCodeAt()` metodu ile her karakterin Unicode değerini alıp ekrana yazdırıyoruz. 

**Örnek 4: Büyük/küçük harf kontrolü**

```javascript
function buyukHarfMi(karakter) {
  const unicodeDegeri = karakter.charCodeAt(0);
  return unicodeDegeri >= 65 && unicodeDegeri <= 90;
}

console.log(buyukHarfMi("A")); // true
console.log(buyukHarfMi("b")); // false
```

Bu örnekte, `buyukHarfMi()` fonksiyonu ile bir karakterin büyük harf olup olmadığını kontrol ediyoruz.  Büyük harflerin Unicode değerleri 65 (A) ile 90 (Z) arasındadır.

**Sonuç**

`charCodeAt()` metodu, string ifadeler üzerinde karakter bazlı işlemler yaparken oldukça kullanışlıdır. Özellikle karakter kodlamaları ile çalışmanız gereken durumlarda bu metodu kullanabilirsiniz. 


## charCodeAt() Metodu: Daha Fazla Örnek

**Örnek 5: Emoji karakterinin Unicode değerini bulma**

```javascript
const emoji = " ";
const unicodeDegeri = emoji.charCodeAt(0);

console.log(unicodeDegeri); // 128512 ( emojisinin Unicode değeri)
```

Bu örnekte, `charCodeAt()` metodunu kullanarak bir emoji karakterinin Unicode değerini nasıl alacağımızı görüyoruz. Emojiler de Unicode karakterlerdir ve kendilerine ait özel Unicode değerlerine sahiptirler.

**Örnek 6: String ifadesindeki tüm karakterlerin Unicode değerlerini bir diziye aktarma**

```javascript
const string = "Merhaba";
const unicodeDegerleri = [];

for (let i = 0; i < string.length; i++) {
  unicodeDegerleri.push(string.charCodeAt(i));
}

console.log(unicodeDegerleri); // [77, 101, 114, 104, 97, 98, 97]
```

Bu örnekte, bir string ifadesindeki tüm karakterlerin Unicode değerlerini alıp yeni bir diziye nasıl ekleyeceğimizi görüyoruz. Bu işlem, karakter kodlamalarıyla çalışırken veya string ifadeleri üzerinde daha kompleks işlemler yaparken faydalı olabilir.

**Örnek 7:  İki string ifadesinin aynı karakterlerden oluşup oluşmadığını kontrol etme (case-insensitive)**

```javascript
function ayniKarakterlerMi(string1, string2) {
  if (string1.length !== string2.length) {
    return false;
  }

  for (let i = 0; i < string1.length; i++) {
    if (string1.charCodeAt(i) !== string2.charCodeAt(i)) {
      return false;
    }
  }

  return true;
}

console.log(ayniKarakterlerMi("merhaba", "MERHABA")); // true
console.log(ayniKarakterlerMi("merhaba", "dünya"));  // false
```

Bu örnekte, `charCodeAt()` metodunu kullanarak iki string ifadesinin aynı karakterlerden oluşup oluşmadığını kontrol eden bir fonksiyon yazıyoruz. Bu fonksiyon, büyük/küçük harf farkını gözetmeksizin çalışır (case-insensitive).

**Örnek 8: String ifadesindeki Türkçe karakterleri sayma**

```javascript
const string = "İstanbul'da bugün hava güzel.";
let turkceKarakterSayisi = 0;

for (let i = 0; i < string.length; i++) {
  const unicodeDegeri = string.charCodeAt(i);

  // Türkçe karakterlerin Unicode aralığı: 286 - 305 (küçük harfler) ve 350 - 355 (büyük harfler)
  if ((unicodeDegeri >= 286 && unicodeDegeri <= 305) || (unicodeDegeri >= 350 && unicodeDegeri <= 355)) {
    turkceKarakterSayisi++;
  }
}

console.log(`"${string}" ifadesinde ${turkceKarakterSayisi} adet Türkçe karakter bulunmaktadır.`);
```

Bu örnekte, `charCodeAt()` metodunu kullanarak bir string ifadesindeki Türkçe karakterleri sayan bir program yazıyoruz.  Türkçe karakterlerin Unicode değer aralığını kullanarak, string içindeki her karakterin Türkçe olup olmadığını kontrol ediyoruz.

Bu örnekler, `charCodeAt()` metodunun farklı senaryolarda nasıl kullanılabileceğini göstermektedir. Unutmayın ki `charCodeAt()` metodu, string ifadeleri üzerinde karakter düzeyinde işlemler yapmanız gereken durumlarda oldukça kullanışlı bir araçtır. 
