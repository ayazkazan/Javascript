## JavaScript String Metodu: split() Kullanım Örnekleri

`split()` metodu, bir stringi belirli bir ayraç kullanarak bir diziye böler. 

**Temel Kullanım:**

```javascript
const metin = "Merhaba,dünya,nasılsın?";
const kelimeler = metin.split(","); // Virgülü ayraç olarak kullan

console.log(kelimeler); // ["Merhaba", "dünya", "nasılsın?"]
```

**Farklı Kullanım Örnekleri:**

**1. Boşluk Karakteriyle Bölme:**

```javascript
const cumle = "Bu bir cümledir.";
const kelimeler = cumle.split(" "); 

console.log(kelimeler); // ["Bu", "bir", "cümledir."]
```

**2. Limit Belirleme:**

`split()` metoduna ikinci bir parametre olarak bölünecek maksimum eleman sayısı verilebilir.

```javascript
const metin = "Elma,Armut,Muz,Çilek";
const meyveler = metin.split(",", 2); // İlk 2 meyveyi al 

console.log(meyveler); // ["Elma", "Armut"]
```

**3. Boş Bir String Kullanarak Her Karakteri Ayırma:**

```javascript
const kelime = "Merhaba";
const harfler = kelime.split(""); 

console.log(harfler); // ["M", "e", "r", "h", "a", "b", "a"]
```

**4. Regex İfadesi Kullanarak Bölme:**

```javascript
const metin = "Elma-Armut Muz,Çilek";
const meyveler = metin.split(/[-,\s]/); // "-", "," veya boşluk karakterleri ile böl

console.log(meyveler); // ["Elma", "Armut", "Muz", "Çilek"]
```

**5. Boş String Döndürme:**

Eğer ayraç olarak boş bir string ("") kullanılırsa, `split()` metodu her karakteri ayrı bir eleman olarak içeren bir dizi döndürür.

```javascript
const kelime = "Merhaba";
const harfler = kelime.split(""); 

console.log(harfler); // ["M", "e", "r", "h", "a", "b", "a"]
```

**Sonuç:**

`split()` metodu, string manipülasyonu için oldukça kullanışlı bir araçtır. Farklı ayraçlar ve sınırlamalar kullanarak stringleri istediğiniz gibi bölebilir ve dizi haline getirebilirsiniz. 
