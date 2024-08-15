## Javascript replace() Methodu Kullanımı ve Örnekler

`replace()` metodu, bir string ifadesi içinde aranan bir değeri, belirtilen bir değerle değiştirir ve yeni bir string döndürür. Orijinal string üzerinde bir değişiklik yapmaz. İki parametre alır:

* **arananDeğer:** Değiştirilecek değer. String veya düzenli ifade (regex) olabilir.
* **yeniDeğer:** Değiştirilecek değerin yerine geçecek değer. Bir string veya bir fonksiyon olabilir.

**Örnekler:**

**1. Basit string değiştirme:**

```javascript
let metin = "Merhaba Dünya!";
let yeniMetin = metin.replace("Dünya", "Mars");
// yeniMetin: "Merhaba Mars!"
```
// **Açıklama:** "Dünya" kelimesi yerine "Mars" kelimesi geçirildi.


**2. İlk eşleşmeyi değiştirme:**

```javascript
let metin = "Bugün hava çok güzel, hava sıcaklığı 25 derece.";
let yeniMetin = metin.replace("hava", "güneş");
// yeniMetin: "Bugün güneş çok güzel, hava sıcaklığı 25 derece."
```
// **Açıklama:** `replace()` metodu varsayılan olarak sadece ilk eşleşmeyi değiştirir. 


**3. Bütün eşleşmeleri değiştirme (regex ile):**

```javascript
let metin = "Bugün hava çok güzel, hava sıcaklığı 25 derece.";
let yeniMetin = metin.replace(/hava/g, "güneş");
// yeniMetin: "Bugün güneş çok güzel, güneş sıcaklığı 25 derece."
```
// **Açıklama:** `/g` (global) flag'i ile bütün "hava" kelimeleri "güneş" ile değiştirilir.


**4. Büyük/küçük harf duyarlılığını kaldırma (regex ile):**

```javascript
let metin = "Merhaba Dünya! dünya nasıl?";
let yeniMetin = metin.replace(/dünya/i, "Mars");
// yeniMetin: "Merhaba Mars! Mars nasıl?"
```
// **Açıklama:** `/i` (case-insensitive) flag'i ile büyük/küçük harf duyarlılığı kaldırılır ve "dünya" kelimesinin tüm varyasyonları "Mars" ile değiştirilir.


**5. Fonksiyon kullanarak dinamik değiştirme:**

```javascript
let metin = "Bugün hava 25 derece, yarın 30 derece olacak.";
let yeniMetin = metin.replace(/(\d+) derece/g, function(eslesme, sicaklik) {
  return (sicaklik * 9/5) + 32 + " Fahrenheit";
});
// yeniMetin: "Bugün hava 77 Fahrenheit, yarın 86 Fahrenheit olacak."
```
// **Açıklama:** `replace()` metodunda bir fonksiyon kullanarak bulunan sayısal değerler (derece cinsinden) Fahrenheit'a çevrilir.


**6. Özel karakterleri escape etme:**

```javascript
let metin = "Fiyat: $10.00";
let yeniMetin = metin.replace(/\$/g, "₺");
// yeniMetin: "Fiyat: ₺10.00"
```
// **Açıklama:** `$` işareti regex'te özel bir anlama geldiği için `\` ile escape edilmesi gerekir.


**7. String'in başlangıcını ve sonunu değiştirme:**

```javascript
let metin = "Merhaba Dünya!";
let yeniMetin = metin.replace(/^/, "Selam ").replace(/!$/, ".");
// yeniMetin: "Selam Merhaba Dünya."
```
// **Açıklama:** `^` string'in başlangıcını, `$` ise string'in sonunu temsil eder.


**8. Birden fazla karakteri tek seferde değiştirme:**

```javascript
let metin = "Bugün hava yağmurlu ve rüzgarlı.";
let yeniMetin = metin.replace(/yağmurlu|rüzgarlı/g, "güneşli");
// yeniMetin: "Bugün hava güneşli ve güneşli."
```
// **Açıklama:** `|` (veya) operatörü ile birden fazla kelime eşleştirilebilir.


**9. HTML etiketlerini kaldırma:**

```javascript
let metin = "Bu bir <b>örnek</b> metindir.";
let yeniMetin = metin.replace(/<\/?[^>]+(>|$)/g, "");
// yeniMetin: "Bu bir örnek metindir."
```
// **Açıklama:** Bu regex ifadesi ile HTML etiketleri string'den kaldırılır.


**10. Unicode karakterleri değiştirme:**

```javascript
let metin = "Bu bir örnek metindir. 🍔";
let yeniMetin = metin.replace(/\u{1F354}/u, "🍕");
// yeniMetin: "Bu bir örnek metindir. 🍕"
```
// **Açıklama:** `\u{UNICODE}` formatı ile Unicode karakterlere erişilebilir. `/u` flag'i ise Unicode modunda çalışmayı sağlar.

Bu örnekler, `replace()` metodunun esnekliğini ve gücünü göstermektedir. Farklı senaryolarda string manipülasyonu için kullanılabilir. 
