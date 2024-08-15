## Javascript Stringlerde `includes()` Metodu

`includes()` metodu, bir stringin içerisinde belirli bir alt dizinin **bulunup bulunmadığını** kontrol etmek için kullanılır. Eğer alt dizi bulunursa `true`, bulunmazsa `false` değerini döndürür.

**Sözdizimi:**

```javascript
string.includes(arananAltDizi, baslangicPozisyonu);
```

* **string:** Aranacak alt diziyi içeren ana string.
* **arananAltDizi:** Aranacak alt dizi.
* **baslangicPozisyonu (opsiyonel):** Aramanın başlayacağı indeks numarası. Varsayılan değeri 0'dır.

**Örnek 1: Basit Bir Kullanım**

```javascript
const mesaj = "Merhaba dünya!";

console.log(mesaj.includes("dünya"));  // true
console.log(mesaj.includes("merhaba")); // false (küçük-büyük harf duyarlı)
```

**Örnek 2: Başlangıç Pozisyonu Kullanımı**

```javascript
const metin = "Bugün hava çok güzel.";

console.log(metin.includes("hava", 5));    // true (5. indexten itibaren arar)
console.log(metin.includes("hava", 10));   // false 
```

**Örnek 3: Bir Dizide Belirli Bir Elemanı Kontrol Etme**

```javascript
const meyveler = ["elma", "armut", "çilek", "muz"];

const istenenMeyve = "çilek";

if (meyveler.includes(istenenMeyve)) {
  console.log(`Evet, ${istenenMeyve} mevcut.`);
} else {
  console.log(`Hayır, ${istenenMeyve} mevcut değil.`);
}
// Çıktı: Evet, çilek mevcut.
```

**Örnek 4: Kullanıcı Girişini Doğrulama**

```javascript
const kullaniciAdi = prompt("Lütfen kullanıcı adınızı girin:");

if (kullaniciAdi.includes(" ")) {
  console.log("Kullanıcı adında boşluk bulunamaz!");
} else {
  console.log("Kullanıcı adı geçerli.");
}
```


**Örnek 5: Bir String Birden Fazla Kelime İçeriyor Mu?**

```javascript
function kelimeleriIceriyorMu(metin, kelimeler) {
  for (const kelime of kelimeler) {
    if (!metin.includes(kelime)) {
      return false;
    }
  }
  return true;
}

const testMetni = "Bu bir Javascript örneğidir.";
const arananKelimeler = ["Javascript", "örnek"];

console.log(kelimeleriIceriyorMu(testMetni, arananKelimeler)); // true
```

**Örnek 6: Dosya Uzantısı Kontrolü**

```javascript
function dosyaTipiGecerliMi(dosyaAdi, izinVerilenUzantılar) {
  const dosyaUzantisi = dosyaAdi.slice(dosyaAdi.lastIndexOf(".") + 1);
  return izinVerilenUzantılar.includes(dosyaUzantisi.toLowerCase());
}

console.log(dosyaTipiGecerliMi("rapor.pdf", ["pdf", "docx"]));   // true
console.log(dosyaTipiGecerliMi("gorsel.png", ["pdf", "docx"]));  // false
```

**Örnek 7: URL Kontrolü**

```javascript
function urlGecerliMi(url) {
  return url.includes("http://") || url.includes("https://");
}

console.log(urlGecerliMi("https://www.ornek.com"));   // true
console.log(urlGecerliMi("www.ornek.com"));           // false
```

**Örnek 8: Büyük/Küçük Harf Duyarlı Olmayan Arama**

`includes()` metodu büyük/küçük harf duyarlıdır. Bunu aşmak için, her iki stringi de `toLowerCase()` veya `toUpperCase()` metodlarıyla aynı duruma getirebilirsiniz:

```javascript
const metin = "Bu bir ÖRNEK metindir.";

console.log(metin.toLowerCase().includes("örnek")); // true
```