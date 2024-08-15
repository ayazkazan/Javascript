## Javascript replaceAll Metodu ve Örnekleri

`replaceAll()` metodu, bir string içindeki **tüm** eşleşmeleri belirtilen bir alt dizeyle değiştirir. 

**Sözdizimi:** 

```javascript
string.replaceAll(aranan, degistirilecek)
```

**Parametreler:**

* **aranan:** Değiştirilecek olan alt dize. Düzenli ifade de olabilir.
* **degistirilecek:** Aranan alt dizenin yerine yazılacak olan yeni dize.

**Geri Dönüş Değeri:** Değiştirilmiş yeni string'i döndürür. Orijinal string'i değiştirmez.

---

**Örnekler:**

**1. Basit Kelime Değiştirme:**

```javascript
const metin = "Elma armut portakal elma armut.";
const yeniMetin = metin.replaceAll("elma", "çilek");
console.log(yeniMetin); // Çilek armut portakal çilek armut. 
```

**Açıklama:** Bu örnekte, "elma" kelimesinin tüm geçtiği yerleri "çilek" ile değiştirdik.

**2. Büyük/Küçük Harfe Duyarlı Değiştirme:**

```javascript
const metin = "Bugün hava çok GÜZEL.";
const yeniMetin = metin.replaceAll("GÜZEL", "güzel");
console.log(yeniMetin); // Bugün hava çok güzel. 
```

**Açıklama:** replaceAll() büyük/küçük harfe duyarlıdır. Sadece birebir eşleşen "GÜZEL" kelimesi değiştirilir.

**3. Düzenli İfade Kullanımı:**

```javascript
const metin = "Telefon numaram: 0555 123 45 67";
const yeniMetin = metin.replaceAll(/\d/g, "*"); 
console.log(yeniMetin); // Telefon numaram: ******** 
```

**Açıklama:** Bu örnekte, düzenli ifade kullanarak tüm rakamları yıldız (*) ile değiştirdik.

**4. Özel Karakterleri Değiştirme:**

```javascript
const metin = "Bu bir örnek! Metin?";
const yeniMetin = metin.replaceAll(/[!?]/g, ".");
console.log(yeniMetin); // Bu bir örnek. Metin.
```

**Açıklama:** Düzenli ifade kullanarak ünlem ve soru işaretini nokta ile değiştirdik.

**5. Birden Fazla Karakter Değiştirme:**

```javascript
const metin = "Bu bir deneme metnidir.";
const yeniMetin = metin.replaceAll("e", "a").replaceAll("i", "u"); 
console.log(yeniMetin); // Bu bur danama matnudur.
```

**Açıklama:** Önce tüm "e" harflerini "a" ile, sonra tüm "i" harflerini "u" ile değiştirdik.

**6. Fonksiyon Kullanarak Değiştirme:**

```javascript
const metin = "Bu bir örnek metin.";
const yeniMetin = metin.replaceAll(" ", (eslesme) => {
  return "-"; 
});
console.log(yeniMetin); // Bu-bir-örnek-metin.
```

**Açıklama:** Boşluk karakterini bulup yerine "-" karakterini koymak için bir fonksiyon kullandık.

**7. Emoji Değiştirme:**

```javascript
const metin = "Merhaba dünya! 😊";
const yeniMetin = metin.replaceAll("😊", "😀");
console.log(yeniMetin); // Merhaba dünya! 😀 
```

**Açıklama:** Emoji karakterlerini de replaceAll() ile değiştirebiliriz.

**8. HTML Etiketi Değiştirme:**

```javascript
const metin = "<strong>Önemli metin</strong>";
const yeniMetin = metin.replaceAll("<strong>", "<b>").replaceAll("</strong>", "</b>");
console.log(yeniMetin); // <b>Önemli metin</b> 
```

**Açıklama:** HTML etiketlerini başka etiketlerle değiştirmek için kullanabiliriz.

**9. URL Düzeltme:**

```javascript
const url = "https://www.örnek.com/dosya adı.pdf";
const yeniUrl = url.replaceAll(" ", "%20");
console.log(yeniUrl); // https://www.örnek.com/dosya%20adı.pdf
```

**Açıklama:** URL'deki boşluk karakterlerini "%20" ile değiştirerek URL'yi düzelttik.

**10. Metin Temizleme:**

```javascript
const metin = " Bu bir   örnek  metin!  ";
const temizMetin = metin.trim().replaceAll(/\s+/g, " ");
console.log(temizMetin); // Bu bir örnek metin!
```

**Açıklama:** `trim()` ile başındaki ve sonundaki boşlukları sildik. Ardından birden fazla boşluk karakterini tek boşluğa indirgedik.

---

Bu örnekler, `replaceAll()` metodunun kullanımına dair temel bilgileri ve farklı senaryolarda nasıl kullanılabileceğini göstermektedir. 
