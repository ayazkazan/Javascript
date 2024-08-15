## Javascript padEnd Metodu ve Örnekleri

`padEnd()` metodu, stringlerin sonuna belirli bir uzunluğa ulaşana kadar verilen bir karakteri veya stringi ekler. 

**Sözdizimi:**

```javascript
string.padEnd(targetLength, padString)
```

**Parametreler:**

* **targetLength:** İstenilen toplam uzunluk. Orijinal string bu uzunluktan kısaysa doldurma işlemi yapılır. 
* **padString (opsiyonel):** Doldurma için kullanılacak string. Varsayılan olarak boşluk (" ") kullanılır. 

**Geri Dönüş Değeri:**

Doldurma işlemi uygulanmış yeni string'i döndürür. Orijinal string'i değiştirmez.

---

**Örnekler:**

**1. Boşluk ile Doldurma:**

```javascript
const str1 = "Merhaba";
const paddedStr1 = str1.padEnd(10); 
console.log(paddedStr1); // "Merhaba   " 
// 3 boşluk ekleyerek toplam uzunluk 10'a ulaştı.
```

**2. Özel Karakter ile Doldurma:**

```javascript
const str2 = "Dünya";
const paddedStr2 = str2.padEnd(10, "*"); 
console.log(paddedStr2); // "Dünya*****" 
// 5 yıldız ekleyerek toplam uzunluk 10'a ulaştı.
```

**3. String İle Doldurma:**

```javascript
const str3 = "JS";
const paddedStr3 = str3.padEnd(10, "-_-"); 
console.log(paddedStr3); // "JS-_-_-_-_" 
// "-_-" stringi tekrarlanarak toplam uzunluk 10'a ulaştı.
```

**4. Hedef Uzunluk Daha Kısa Olursa:**

```javascript
const str4 = "Javascript";
const paddedStr4 = str4.padEnd(5, "!");
console.log(paddedStr4); // "Javascript" 
// Hedef uzunluk orijinal stringden kısa olduğu için değişiklik olmadı.
```

**5. Sayılarla Kullanım:**

```javascript
const num = 123;
const paddedNum = num.toString().padEnd(5, "0"); 
console.log(paddedNum); // "12300"
// Sayıyı stringe çevirip 2 adet "0" ekleyerek toplam uzunluk 5'e ulaştı.
```

**6. Emoji ile Doldurma:**

```javascript
const str6 = "Tebrikler";
const paddedStr6 = str6.padEnd(15, "🎉");
console.log(paddedStr6); // "Tebrikler🎉🎉🎉🎉"
// 4 adet 🎉 emojisi ekleyerek toplam uzunluk 15'e ulaştı.
```

**7. Türkçe Karakterlerle Kullanım:**

```javascript
const str7 = "Merhaba";
const paddedStr7 = str7.padEnd(12, "ğ");
console.log(paddedStr7); // "Merhabağğğğğ" 
// 5 adet "ğ" harfi ekleyerek toplam uzunluk 12'ye ulaştı.
```

**8. Boş String ile Doldurma:**

```javascript
const str8 = "Test";
const paddedStr8 = str8.padEnd(10, "");
console.log(paddedStr8); // "Test" 
// Boş string ile doldurma yapıldığında değişiklik olmaz.
```

**9. Birden Fazla Karakter Ekleme:**

```javascript
const str9 = "Kod";
const paddedStr9 = str9.padEnd(10, "yaz ");
console.log(paddedStr9); // "Kodyaz yaz " 
// "yaz " stringi tekrarlanarak toplam uzunluk 10'a ulaştı.
```

**10. Uygulama İçi Örnek:**

```javascript
const usernames = ["ali", "veli", "ahmet"];
const maxLength = 10;

const formattedUsernames = usernames.map(username => {
  return username.padEnd(maxLength, ".");
});

console.log(formattedUsernames); 
// ["ali.......", "veli......", "ahmet....."] 
// Kullanıcı adlarını 10 karaktere tamamlamak için "." ile doldurdu.
```

Bu örneklerde `padEnd` metodunun farklı kullanım şekillerini ve olası çıktıları gördük. 
