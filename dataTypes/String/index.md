## JavaScript'te String: Metinleri Anlamak ve Kullanmak

JavaScript'te, metinleri temsil etmek ve üzerinde işlem yapmak için kullanılan temel veri tiplerinden biri **string**'dir. Stringler, tek tırnak (`'`) veya çift tırnak (`"`) yada (``) içine alınmış karakter dizileridir. 

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
