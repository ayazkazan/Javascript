## JavaScript'te String: Metinleri Anlamak ve Kullanmak

JavaScript'te, metinleri temsil etmek ve üzerinde işlem yapmak için kullanılan temel veri tiplerinden biri **string**'dir. Stringler, tek tırnak (`'`) veya çift tırnak (`"`) içine alınmış karakter dizileridir. 

**String'lerin Özellikleri:**

* **Değiştirilemez (Immutable):** Bir string oluşturduktan sonra, bireysel karakterlerini doğrudan değiştiremezsiniz. String'ler üzerinde işlem yaptığınızda, yeni bir string oluşturulur ve bu, orijinal stringi etkilemez.
* **Diziler Gibi:** Stringler, her bir karakteri bir dizi gibi işleyebileceğiniz sıralı bir karakter dizisidir.
* **Unicode Desteği:** JavaScript, Unicode karakter setini destekler, bu da dünyanın hemen hemen tüm yazı sistemlerini temsil edebildiği anlamına gelir.

**String Oluşturma Örnekleri:**

```javascript
// Tek tırnak ile string oluşturma
let selamlama = 'Merhaba Dünya!';

// Çift tırnak ile string oluşturma
let mesaj = "Bugün hava çok güzel.";

// Boş bir string oluşturma
let bosString = '';

// Özel karakter içeren string oluşturma
let email = "info@example.com"; 
```

**String Methodları: Metinleri Manipüle Etmek**

JavaScript'in stringleri işlemek için sunduğu çok çeşitli yöntemler vardır. İşte en yaygın olarak kullanılanları:

**1. Uzunluk ve İndeksleme:**

* **`length`:** Stringin karakter sayısını (uzunluğunu) döndürür.

```javascript
let selamlama = 'Merhaba Dünya!';
console.log(selamlama.length); // 14
```

* **`charAt(index)`:** Belirtilen indeksteki karakteri döndürür. İndeks 0'dan başlar.

```javascript
let selamlama = 'Merhaba Dünya!';
console.log(selamlama.charAt(0)); // "M"
console.log(selamlama.charAt(7)); // "D"
```

**2. Arama ve Değiştirme:**

* **`indexOf(searchValue, fromIndex)`:** String içinde belirtilen değerin ilk geçtiği indeksi döndürür. Bulunamazsa -1 döndürür. `fromIndex` isteğe bağlıdır ve aramanın başlayacağı indeksi belirtir.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.indexOf("hava")); // 7
console.log(metin.indexOf("yağmur")); // -1
```

* **`lastIndexOf(searchValue, fromIndex)`:** String içinde belirtilen değerin son geçtiği indeksi döndürür. Bulunamazsa -1 döndürür. `fromIndex` isteğe bağlıdır ve aramanın başlayacağı indeksi belirtir (tersten).

```javascript
let metin = "Bugün hava çok güzel. Hava çok güzel.";
console.log(metin.lastIndexOf("güzel")); // 24
```

* **`includes(searchString, position)`:** Stringin belirtilen değeri içerip içermediğini kontrol eder ve true veya false döndürür.  `position` isteğe bağlıdır ve aramanın başlayacağı indeksi belirtir.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.includes("hava")); // true
console.log(metin.includes("yağmur")); // false
```

* **`startsWith(searchString, position)`:** Stringin belirtilen değer ile başlayıp başlamadığını kontrol eder ve true veya false döndürür.  `position` isteğe bağlıdır ve aramanın başlayacağı indeksi belirtir.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.startsWith("Bugün")); // true
console.log(metin.startsWith("hava")); // false
```

* **`endsWith(searchString, length)`:** Stringin belirtilen değer ile bitip bitmediğini kontrol eder ve true veya false döndürür. `length` isteğe bağlıdır ve stringin uzunluğunu sınırlandırır.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.endsWith("güzel.")); // true
console.log(metin.endsWith("hava")); // false
```

* **`replace(searchValue, replaceValue)`:** String içinde belirtilen değeri arar ve bulduğu ilk değeri, belirtilen yeni değerle değiştirir.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.replace("güzel", "harika")); // "Bugün hava çok harika."
```

* **`replaceAll(searchValue, replaceValue)`:** String içinde belirtilen değeri arar ve bulduğu tüm değerleri, belirtilen yeni değerle değiştirir.

```javascript
let metin = "Bugün hava çok güzel. Hava çok güzel.";
console.log(metin.replaceAll("güzel", "harika")); // "Bugün hava çok harika. Hava çok harika."
```

**3. String Kesme ve Birleştirme:**

* **`substring(startIndex, endIndex)`:** Stringin belirtilen indeksler arasındaki bölümünü yeni bir string olarak döndürür. `endIndex` isteğe bağlıdır ve belirtilmezse stringin sonuna kadar gider.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.substring(7, 11)); // "hava"
console.log(metin.substring(12)); // "çok güzel."
```

* **`slice(startIndex, endIndex)`:** `substring` ile benzerdir, ancak negatif indeksleri destekler. Negatif indeks, stringin sonundan itibaren saymaya başlar.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.slice(7, 11)); // "hava"
console.log(metin.slice(12)); // "çok güzel."
console.log(metin.slice(-6)); // "güzel."
```

* **`split(separator, limit)`:** Stringi belirtilen ayırıcıya göre bölerek bir dizi döndürür. `limit` isteğe bağlıdır ve döndürülecek maksimum eleman sayısını belirtir.

```javascript
let metin = "Elma,Armut,Muz";
console.log(metin.split(",")); // ["Elma", "Armut", "Muz"]
console.log(metin.split(",", 2)); // ["Elma", "Armut"]
```

* **`concat(string1, ..., stringN)`:** İki veya daha fazla stringi birleştirir.

```javascript
let selamlama = "Merhaba";
console.log(selamlama.concat(" ", "dünya!")); // "Merhaba dünya!"
```

**4. Büyük/Küçük Harf Dönüşümü:**

* **`toUpperCase()`:** Stringin tüm karakterlerini büyük harfe dönüştürür.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.toUpperCase()); // "BUGÜN HAVA ÇOK GÜZEL."
```

* **`toLowerCase()`:** Stringin tüm karakterlerini küçük harfe dönüştürür.

```javascript
let metin = "Bugün hava çok güzel.";
console.log(metin.toLowerCase()); // "bugün hava çok güzel."
```

**5. Boşluk İşlemleri:**

* **`trim()`:** Stringin başındaki ve sonundaki boşlukları siler.

```javascript
let metin = "   Bugün hava çok güzel.   ";
console.log(metin.trim()); // "Bugün hava çok güzel."
```

**6. Tekrarlama ve Doldurma:**

* **`repeat(count)`:** Stringi belirtilen sayıda tekrarlar. 

```javascript
let metin = "na";
console.log(metin.repeat(3)); // "nanana"
```

* **`padStart(targetLength, padString)`:** Stringin başına, belirtilen uzunluğa ulaşana kadar belirtilen stringi ekler. 

```javascript
let metin = "5";
console.log(metin.padStart(4, "0")); // "0005"
```

* **`padEnd(targetLength, padString)`:** Stringin sonuna, belirtilen uzunluğa ulaşana kadar belirtilen stringi ekler. 

```javascript
let metin = "5";
console.log(metin.padEnd(4, "0")); // "5000"
```

**Önemli Notlar:**

* Stringler değiştirilemez (immutable) verilerdir. Yani, bir string üzerinde bir method çalıştırdığınızda, orijinal string değiştirilmez, yeni bir string oluşturulur.
* String methodları, orijinal stringi değiştirmez, yeni bir string döndürür. Bu nedenle, sonucu yeni bir değişkene atamanız gerekebilir.

**Stringleri Daha İyi Anlamak:**

* **Stringlerin İntern Temsili:** JavaScript, stringleri UTF-16 kodlama şemasında 16 bitlik karakterlerden oluşan bir dizi olarak depolar. Bu, stringlerin, farklı diller ve karakter kümeleri için yeterli bir temsil sağlar.
* **Stringler ve Bellek:** Stringler, Javascript'in heap bellek alanında depolanır. Uzun stringler daha fazla bellek kullanır.

**Sonuç:**

Stringler, JavaScript'in metinleri temsil etmek ve işlemek için kullandığı temel yapı taşlarıdır. Bu methodlar sayesinde, çeşitli web uygulamalarında metinleri manipüle etmek, düzenlemek, analiz etmek ve görüntülemek için güçlü araçlara sahipsiniz.
