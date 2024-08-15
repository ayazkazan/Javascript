## JavaScript String indexOf() Metodu: Kullanım ve Örnekler

`indexOf()` metodu, bir string içinde belirli bir alt dizeyi arar ve ilk eşleşmenin başlangıç indeksini döndürür. Alt dize bulunamazsa, -1 değerini döndürür. 

**Sözdizimi:**

```javascript
string.indexOf(arananAltDize, başlangıçİndeksi)
```

**Parametreler:**

* **arananAltDize:** Aranacak alt dize.
* **başlangıçİndeksi (opsiyonel):** Aramanın başlayacağı indeks. Varsayılan değeri 0'dır.

**Dönüş Değeri:**

* İlk eşleşmenin başlangıç indeksi (0 tabanlı indeksleme).
* Eşleşme yoksa -1.

**Örnekler:**

**1. Basit Bir Kullanım:**

```javascript
const metin = "Merhaba dünya!";
const indeks = metin.indexOf("dünya");
console.log(indeks); // Çıktı: 7
```

**2. Alt Dize Bulunamazsa:**

```javascript
const metin = "Merhaba dünya!";
const indeks = metin.indexOf("merhaba");
console.log(indeks); // Çıktı: -1 (büyük/küçük harf duyarlı)
```

**3. Başlangıç İndeksi Belirleme:**

```javascript
const metin = "Merhaba dünya, dünya!";
const indeks = metin.indexOf("dünya", 8); // 8. indeksten itibaren ara
console.log(indeks); // Çıktı: 15
```

**4. Birden Fazla Eşleşmede İlk Eşleşmenin İndeksi:**

```javascript
const metin = "Merhaba dünya, dünya!";
const indeks = metin.indexOf("dünya");
console.log(indeks); // Çıktı: 7 (ilk "dünya" kelimesinin indeksi)
```

**5. indexOf() ile Döngü Kullanımı:**

```javascript
const metin = "Bu bir cümle. Bu da başka bir cümle.";
let indeks = metin.indexOf("Bu");

while (indeks !== -1) {
  console.log(`"Bu" kelimesi ${indeks}. indekste bulundu.`);
  indeks = metin.indexOf("Bu", indeks + 1); // Bir sonraki "Bu" kelimesini ara
}
```
**Çıktı:**
```
"Bu" kelimesi 0. indekste bulundu.
"Bu" kelimesi 14. indekste bulundu.
```

