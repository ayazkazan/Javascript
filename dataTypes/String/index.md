## JavaScript'te String: Metinleri Anlamak ve Kullanmak

JavaScript'te, metinleri temsil etmek ve üzerinde işlem yapmak için kullanılan temel veri tiplerinden biri **string**'dir. Stringler, tek tırnak (`'`) veya çift tırnak (`"`) yada backtick (`) içine alınmış karakter dizileridir. 

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

// Backtick ile string oluşturma
let string3 = `Merhaba Dünya`;

// Boş bir string oluşturma
let bosString = '';

// Özel karakter içeren string oluşturma
let email = "info@example.com"; 
```



**String methodlarının bir listesi:**

1. charAt()
2. charCodeAt()
3. concat()
4. endsWith()
5. includes()
6. indexOf()
7. lastIndexOf()
8. localeCompare()
9. match()
10. padEnd()
11. padStart()
12. repeat()
13. replace()
14. replaceAll()
15. search()
16. slice()
17. split()
18. startsWith()
19. substr()
20. substring()
21. toLowerCase()
22. toUpperCase()
23. trim()
24. trimStart()
25. trimEnd()
26. valueOf()

Bu liste, JavaScript'teki temel string methodlarını içerir. Her methodun belirli bir işlevi vardır ve stringleri manipüle etmek veya onlar hakkında bilgi almak için kullanılır.

