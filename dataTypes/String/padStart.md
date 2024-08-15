## Javascript String padStart Metodu ve Örnekleri

`padStart()` metodu, bir stringin başına belirtilen bir uzunluğa ulaşana kadar belirtilen bir karakteri veya stringi ekler. 

**Sözdizimi:**

```javascript
string.padStart(targetLength, padString)
```

**Parametreler:**

* **targetLength:** Hedef uzunluk. Stringin ulaşması gereken uzunluk.
* **padString (opsiyonel):** Dolgu stringi. Stringin başına eklemek istediğiniz karakter veya string. Varsayılan değeri boşluktur (" ").

**Geri Dönüş Değeri:**

* Dolgulmuş yeni bir string döndürür. Orijinal string değiştirilmez.

**Örnekler:**

**1. Sayıların Hizalanması:**

```javascript
let sayi1 = "15";
let sayi2 = "5";

let hizalanmisSayi1 = sayi1.padStart(2, "0"); // Hedef uzunluk 2, dolgu "0"
let hizalanmisSayi2 = sayi2.padStart(2, "0"); 

console.log(hizalanmisSayi1); // "15"  
console.log(hizalanmisSayi2); // "05"  
```

**2. Kredi Kartı Numarası Formatlama:**

```javascript
let krediKarti = "1234567890123456";
let formatlanmisKrediKarti = krediKarti.padStart(19, "*"); // Hedef uzunluk 19, dolgu "*"

console.log(formatlanmisKrediKarti); // "****1234567890123456"  
```

**3. Tarih Formatlama:**

```javascript
let gun = "5";
let ay = "9";
let yil = "2023";

let formatlanmisGun = gun.padStart(2, "0");
let formatlanmisAy = ay.padStart(2, "0");

console.log(`${formatlanmisGun}.${formatlanmisAy}.${yil}`); // "05.09.2023"  
```

**4. Boşluk Ekleme:**

```javascript
let metin = "Merhaba";
let hizalanmisMetin = metin.padStart(10, " "); // Hedef uzunluk 10, dolgu " "

console.log(hizalanmisMetin); // "   Merhaba" 
```

**5. Özel Karakterlerle Dolgu:**

```javascript
let isim = "Ali";
let cizgiliIsim = isim.padStart(10, "-"); // Hedef uzunluk 10, dolgu "-"

console.log(cizgiliIsim); // "-------Ali" 
```

**6. String Birleştirme:**

```javascript
let ad = "John";
let soyad = "Doe";
let tamAd = `${soyad.padStart(10, ".")} ${ad}`; 

console.log(tamAd); // ".......Doe John" 
```

**7. Dosya Adı Oluşturma:**

```javascript
let dosyaNo = "123";
let dosyaAdi = `dosya_${dosyaNo.padStart(4, "0")}.txt`; // Hedef uzunluk 4, dolgu "0"

console.log(dosyaAdi); // "dosya_0123.txt" 
```

**8. İlerleme Çubuğu Oluşturma:**

```javascript
let yuzde = 75;
let bar = "#".repeat(yuzde).padEnd(100, " ");

console.log(bar); // "#########################                                                                        " 
```

**9. Tablo Hücresi Hizalama:**

```javascript
let urun1 = "Elma";
let urun2 = "Muz";
let urun3 = "Çilek";

let hizalanmisUrun1 = urun1.padStart(10, " ");
let hizalanmisUrun2 = urun2.padStart(10, " ");
let hizalanmisUrun3 = urun3.padStart(10, " ");

console.log(`${hizalanmisUrun1} | ${hizalanmisUrun2} | ${hizalanmisUrun3}`);
//       Elma |       Muz |     Çilek 
```

**10. Telefon Numarası Formatlama:**

```javascript
let telNo = "5551234567";
let formatlanmisTelNo = telNo.padStart(10, "0");

console.log(`(5${formatlanmisTelNo.slice(3, 6)}) ${formatlanmisTelNo.slice(6, 9)}-${formatlanmisTelNo.slice(9)}`); 
// (555) 123-4567
```

Bu örnekler, `padStart()` metodunun stringleri formatlarken ve hizalarken ne kadar kullanışlı olduğunu göstermektedir. 
