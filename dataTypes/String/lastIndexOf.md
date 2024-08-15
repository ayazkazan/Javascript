## Javascript lastIndexOf() Methodu

`lastIndexOf()` metodu, bir dizede belirli bir karakterin veya alt dizenin **son** geçtiği indeksi (konumu) bulmak için kullanılır. Aranan karakter veya alt dize bulunamazsa, metot `-1` döndürür.

**Sözdizimi:**

```javascript
dizi.lastIndexOf(aranan, [başlangıçIndeksi])
```

* **aranan:** Aranacak karakter veya alt dize.
* **başlangıçIndeksi (isteğe bağlı):** Aramanın başlayacağı indeksi belirtir. Belirtilmezse, arama dizenin sonundan başlar.

**Örnekler:**

**1. Basit Kullanım:**

```javascript
let metin = "Merhaba Dünya!";
let sonIndeks = metin.lastIndexOf("a");

console.log(sonIndeks); // Çıktı: 9
```

Bu örnekte, "a" karakterinin son geçtiği indeksi bulduk. "a" karakteri 9. indekste olduğu için sonuç `9` olacaktır.

**2. Başlangıç İndeksi Kullanımı:**

```javascript
let metin = "Merhaba Dünya!";
let sonIndeks = metin.lastIndexOf("a", 5);

console.log(sonIndeks); // Çıktı: 3
```

Bu örnekte, aramayı 5. indeksten başlattık. Bu nedenle, "a" karakterinin 5. indeksten önceki son geçtiği indeksi (3. indeks) bulduk.

**3. Alt Dize Arama:**

```javascript
let metin = "Bu bir örnek metindir.";
let sonIndeks = metin.lastIndexOf("bir");

console.log(sonIndeks); // Çıktı: 4
```

Bu örnekte, "bir" alt dizisinin son geçtiği indeksi bulduk. Sonuç `4` olacaktır.

**4. Bulunamayan Karakter:**

```javascript
let metin = "Merhaba Dünya!";
let sonIndeks = metin.lastIndexOf("z");

console.log(sonIndeks); // Çıktı: -1
```

Bu örnekte, "z" karakteri metinde bulunmadığı için sonuç `-1` olacaktır.

**5. Gerçek Hayat Örneği:**

Bir web sitesinin URL'sinde dosya uzantısını bulmak için `lastIndexOf()` metodunu kullanabiliriz:

```javascript
let url = "https://www.ornek.com/dosyalar/resim.jpg";
let uzantiBaslangic = url.lastIndexOf(".") + 1;
let uzanti = url.slice(uzantiBaslangic);

console.log(uzanti); // Çıktı: "jpg"
```

Bu örnekte, URL'de son "." karakterinin indeksini bulduk ve bu indeksten sonraki kısmı alarak dosya uzantısını elde ettik.

Bu örnekler, `lastIndexOf()` metodunun farklı kullanım senaryolarını göstermektedir. Bu metodu, dizelerde belirli karakterlerin veya alt dizelerin konumlarını bulmak için kullanabilirsiniz.
