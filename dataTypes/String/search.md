## Javascript String Search Metodu Örnekleri

`search()` metodu, bir string içerisinde belirli bir değeri (regex veya string) arar ve ilk eşleşmenin **index** numarasını döndürür. Eşleşme bulunamazsa **-1** değerini döndürür.

**Genel Kullanım:**

```javascript
string.search(arananDeğer);
```

**Örnekler:**

**1. Basit String Arama:**

```javascript
const metin = "Merhaba Dünya!";
const sonuc = metin.search("Dünya"); 
console.log(sonuc); // 7 (Çünkü "Dünya" kelimesi 7. indexten başlıyor)
```

**2. Büyük/Küçük Harf Duyarlılığı:**

```javascript
const metin = "Merhaba Dünya!";
const sonuc = metin.search("dünya"); 
console.log(sonuc); // -1 (Çünkü "dünya" kelimesi küçük harfle yazıldı, eşleşme yok)
```

**3. Regex Kullanımı:**

```javascript
const metin = "Bugün hava 25 derece.";
const sonuc = metin.search(/\d+/); // Herhangi bir rakam için regex kullanımı
console.log(sonuc); // 14 (İlk rakam 14. indexte)
```

**4. Özel Karakter Arama:**

```javascript
const metin = "Javascript öğrenmek çok eğlenceli!";
const sonuc = metin.search("!"); 
console.log(sonuc); // 29 ("!" karakteri 29. indexte)
```

**5. Birden Fazla Eşleşme Durumunda:**

```javascript
const metin = "Bugün hava çok güzel, yarın da güzel olacak.";
const sonuc = metin.search("güzel");
console.log(sonuc); // 14 (İlk "güzel" kelimesinin indexi döndürülür)
```

**6. Boş String Arama:**

```javascript
const metin = "Merhaba Dünya!";
const sonuc = metin.search("");
console.log(sonuc); // 0 (Boş string her zaman 0. indexte bulunur)
```

**7. String Olmayan Değer Arama:**

```javascript
const metin = "1234567890";
const sonuc = metin.search(123); // Sayısal değer string olarak algılanır
console.log(sonuc); // 0 ("123" stringi 0. indexten başlıyor)
```

**8. Türkçe Karakter Desteği:**

```javascript
const metin = "İstanbul'a hoş geldiniz!";
const sonuc = metin.search("İstanbul");
console.log(sonuc); // 0 ("İstanbul" kelimesi 0. indexten başlıyor)
```

**9. Unicode Karakter Arama:**

```javascript
const metin = "Mutlu Yıllar! \u{1F389}"; // Balon emojisi
const sonuc = metin.search("\u{1F389}");
console.log(sonuc); // 12 (Emoji 12. indexte)
```

**10. Nesne Özelliği Olarak Kullanım:**

```javascript
const kullanici = {
  ad: "Ahmet",
  soyad: "Yılmaz"
};

const sonuc = kullanici.ad.search("met"); // Nesne özelliği üzerinde arama
console.log(sonuc); // 2 ("met" stringi 2. indexten başlıyor)
```

**Sonuç:**

`search()` metodu, stringler içerisinde arama yapmak için pratik bir yöntem sunar. Hem basit string hem de regex ifadeleriyle çalışabilir ve ilk eşleşmenin index numarasını döndürür. Bu örnekler, `search()` metodunun farklı kullanım senaryolarını ve dikkat edilmesi gereken noktaları göstermektedir. 
