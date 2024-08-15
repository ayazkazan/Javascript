## Javascript Stringlerde concat() Metodu

`concat()` metodu, iki veya daha fazla stringi birleştirerek yeni bir string döndürür. Orijinal stringler üzerinde değişiklik yapmaz. 

**Temel Kullanım:**

```javascript
string1.concat(string2, string3, ..., stringN)
```

**Örnekler:**

**1. İki Stringi Birleştirme:**

```javascript
let isim = "Ahmet";
let soyisim = "Yılmaz";

let tamIsim = isim.concat(" ", soyisim);

console.log(tamIsim); // Çıktı: "Ahmet Yılmaz"
```

**2. Birden Fazla Stringi Birleştirme:**

```javascript
let kelime1 = "Merhaba";
let kelime2 = "dünya";
let kelime3 = "!";

let cumle = kelime1.concat(" ", kelime2, kelime3);

console.log(cumle); // Çıktı: "Merhaba dünya!"
```

**3. Değişkenler ve String Literalleri:**

```javascript
let website = "www.";
let domain = "google.com";

let url = "https://".concat(website, domain);

console.log(url); // Çıktı: "https://www.google.com"
```

**4. Sayıları String Olarak Birleştirme:**

```javascript
let sayi1 = 10;
let sayi2 = 25;

// Sayıları string olarak birleştirmek için toString() metodunu kullanabiliriz.
let toplam = sayi1.toString().concat("+", sayi2.toString(), "=", (sayi1 + sayi2));

console.log(toplam); // Çıktı: "10+25=35"
```

**Alternatif: + Operatörü**

String birleştirme için `concat()` metodu yerine `+` operatörünü de kullanabilirsiniz. 

```javascript
let isim = "Ayşe";
let soyisim = "Kara";

let tamIsim = isim + " " + soyisim;

console.log(tamIsim); // Çıktı: "Ayşe Kara"
```

**Önemli Notlar:**

* `concat()` metodu her zaman yeni bir string döndürür. Orijinal stringler değişmeden kalır.
* Performans açısından `concat()` metodu yerine `+` operatörünü kullanmak daha verimlidir.
* `concat()` metodu, argüman olarak array almaz. Bir array içindeki stringleri birleştirmek için `join()` metodunu kullanabilirsiniz.


Umarım bu örnekler `concat()` metodunun kullanımını anlamanıza yardımcı olmuştur.
