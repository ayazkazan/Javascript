Elbette, JavaScript'te `endsWith()` yönteminin nasıl kullanılacağını buradayım.

`endsWith()` yöntemi, verilen bir alt dizgiyle bitip bitmediğini belirleyerek bir dizeyi kontrol eder ve bir eşleşme bulunursa `true`, aksi takdirde `false` döndürür. Büyük/küçük harfe duyarlıdır.

İşte sözdizimi:

```javascript
string.endsWith(searchString, length)
```

* `searchString`: Aranacak alt dize.
* `length` (isteğe bağlı): `string`in kontrol edilecek uzunluğu. Varsayılan değer, `string`in uzunluğudur.

Şimdi bazı örneklere bakalım:

**Örnek 1: Basit kullanım**

```javascript
const string = "Merhaba dünya!";

console.log(string.endsWith("dünya!")); // true
console.log(string.endsWith("Merhaba")); // false
```

**Örnek 2: Büyük/küçük harfe duyarlılık**

```javascript
const string = "JavaScript Eğlencelidir";

console.log(string.endsWith("Eğlencelidir")); // true
console.log(string.endsWith("eğlencelidir")); // false
```

**Örnek 3: `length` parametresinin kullanımı**

```javascript
const string = "Merhaba gezegen!";

console.log(string.endsWith("gezegen", 12)); // true
```

Bu örnekte `endsWith()` yöntemi, `string`in ilk 12 karakterini ("Merhaba gezegen") kontrol eder ve "gezegen" ile bitip bitmediğini görür.

**Örnek 4: Boş bir dize ile kullanma**

```javascript
const string = "Merhaba dünya!";

console.log(string.endsWith("")); // true
```

Bu, `endsWith()` yönteminin her zaman boş bir dizeyle biteceği için `true` döndüreceği anlamına gelir.

Bunlar, JavaScript'te `endsWith()` yönteminin nasıl kullanılacağına dair sadece birkaç örnektir.

Umarım bu yardımcı olur! Başka sorularınız varsa bana bildirin.
