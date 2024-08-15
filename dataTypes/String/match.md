## Javascript Stringlerde match() Methodu

`match()` metodu, bir dize içerisinde belirli bir kalıbı arar ve eşleşme durumunda bulunan sonuçları bir dizi olarak döndürür. Kalıp, bir düzenli ifade (regex) veya bir dize olabilir.

**Temel Kullanım:**

```javascript
const string = "Merhaba Dünya!";
const regex = /Dünya/g;
const sonuc = string.match(regex);

console.log(sonuc); // ["Dünya"]
```

**Örnekler:**

**1. Bir kelimeyi bulma:**

```javascript
const metin = "Bugün hava çok güzel.";
const kelime = "güzel";

const sonuc = metin.match(kelime); 

console.log(sonuc); // ["güzel", index: 16, input: "Bugün hava çok güzel.", groups: undefined]
```

Bu örnekte, "güzel" kelimesi metin içerisinde aranmış ve bulunan ilk eşleşmenin bilgileri bir dizi olarak döndürülmüştür.

**2. Birden fazla eşleşmeyi bulma (Global Flag ile):**

```javascript
const metin = "Elma, armut, muz, elma, portakal";
const regex = /elma/gi; // "g" flag'i tüm eşleşmeleri bulur, "i" flag'i büyük/küçük harf duyarlılığını kaldırır.

const sonuc = metin.match(regex); 

console.log(sonuc); // ["Elma", "elma"]
```

Bu örnekte, "elma" kelimesi metin içerisinde aranmış ve bulunan tüm eşleşmeler bir dizi olarak döndürülmüştür. "g" flag'i kullanılmasaydı sadece ilk eşleşme bulunacaktı.

**3. Bir sayı aralığını bulma:**

```javascript
const metin = "Bugün 10 derece, yarın 15 derece";
const regex = /[1-9][0-9]/g; // 10 ile 99 arasındaki sayıları bulur.

const sonuc = metin.match(regex); 

console.log(sonuc); // ["10", "15"]
```

Bu örnekte, 10 ile 99 arasındaki sayılar metin içerisinde aranmış ve bulunan tüm eşleşmeler bir dizi olarak döndürülmüştür.

**4. Eşleşme Bulunamaması:**

```javascript
const metin = "Merhaba Dünya!";
const regex = /Ay/g;
const sonuc = metin.match(regex);

console.log(sonuc); // null
```

Bu örnekte, "Ay" kelimesi metin içerisinde bulunmadığı için `match()` metodu `null` değerini döndürür.

**Sonuç:**

`match()` metodu, Javascript'te stringler üzerinde düzenli ifadeler kullanarak arama yapmak için kullanışlı bir yöntemdir. Farklı flag'ler ve regex kalıpları kullanarak çeşitli arama işlemleri gerçekleştirmenizi sağlar. 
