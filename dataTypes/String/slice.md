## Javascript Stringlerde Slice Metodu ve Örnek Kullanımlar

`slice()` metodu, bir stringin belirtilen bir bölümünü kopyalayarak yeni bir string döndürür. 

**Kullanımı:**

```javascript
string.slice(başlangıçIndeksi, bitişIndeksi);
```

**Parametreler:**

* **başlangıçIndeksi:** Kopyalamanın başlayacağı indeks. (Dahil)
* **bitişIndeksi:** Kopyalamanın biteceği indeks. (Hariç) Eğer belirtilmezse stringin sonuna kadar kopyalar.

**Not:**

* Orijinal stringi değiştirmez.
* İndeksler negatif olabilir, bu durumda stringin sonundan itibaren sayılır.

---

**Örnekler:**

**1. Baştan Belirli Bir Kısmı Almak:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(0, 7);
console.log(yeniStr); // Çıktı: Merhaba 
```
> **Açıklama:** Stringin 0. indeksinden başlayarak 7. indekse kadar (7. indeks hariç) kopyaladık.

**2. Belirli Bir İndeksten Sonraki Kısmı Almak:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(8); 
console.log(yeniStr); // Çıktı: Dünya!
```
> **Açıklama:** 8. indeksten başlayarak stringin sonuna kadar kopyaladık. 

**3. Belirli Bir Aralığı Almak:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(3, 9);
console.log(yeniStr); // Çıktı: haba D
```
> **Açıklama:** 3. indeksten başlayarak 9. indekse kadar (9. indeks hariç) kopyaladık.

**4. Negatif Başlangıç İndeksi Kullanmak:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(-6);
console.log(yeniStr); // Çıktı: Dünya!
```
> **Açıklama:** Stringin sonundan 6 karakter geriye giderek sonuna kadar kopyaladık.

**5. Negatif Bitiş İndeksi Kullanmak:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(0, -7);
console.log(yeniStr); // Çıktı: Merhaba
```
> **Açıklama:** Stringin başından başlayarak sondan 7 karakter öncesine kadar kopyaladık.

**6. Hem Negatif Başlangıç Hem de Bitiş İndeksi Kullanmak:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(-6, -1);
console.log(yeniStr); // Çıktı: Dünya
```
> **Açıklama:** Sondan 6. indeksten başlayarak sondan 1. indekse kadar (1. indeks hariç) kopyaladık.

**7. Boş String Döndürmek:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(5, 5);
console.log(yeniStr); // Çıktı:  (Boş string)
```
> **Açıklama:** Başlangıç ve bitiş indeksleri aynı olduğunda boş string döndürür.

**8. Başlangıç İndeksi Bitiş İndeksinden Büyük Olduğunda:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(7, 2);
console.log(yeniStr); // Çıktı:  (Boş string)
```
> **Açıklama:** Başlangıç indeksi bitiş indeksinden büyük olduğunda boş string döndürür.

**9. String Kopyalamak:**

```javascript
const str = "Merhaba Dünya!";
const yeniStr = str.slice(); 
console.log(yeniStr); // Çıktı: Merhaba Dünya!
```
> **Açıklama:** Herhangi bir parametre girilmediğinde stringin tamamını kopyalar. 

**10. Türkçe Karakterlerle Kullanım:**

```javascript
const str = "Çalışkan Şöför";
const yeniStr = str.slice(0, 8);
console.log(yeniStr); // Çıktı: Çalışkan 
```
> **Açıklama:** Türkçe karakterler de indekslere dahil edilir ve slice metodu doğru çalışır.
