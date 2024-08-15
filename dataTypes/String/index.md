### JavaScript'te String Tanımı

JavaScript'te `String`, metin verilerini (karakter dizilerini) temsil eden bir veri türüdür. String'ler, bir veya birden fazla karakterden oluşabilir ve tek tırnak (`'...'`), çift tırnak (`"..."`), veya backtick (`\`...\``) ile tanımlanabilirler.

```javascript
let string1 = 'Merhaba';
let string2 = "Dünya";
let string3 = `Merhaba Dünya`;
```

### JavaScript String Metotları

JavaScript `String` nesnesi, metin üzerinde işlem yapmak için birçok yerleşik metoda sahiptir. İşte en yaygın kullanılan bazı string metotları:

#### 1. **`charAt(index)`**
   - Belirtilen indeksteki karakteri döndürür.
   - Örnek: `'Merhaba'.charAt(1)` // "e"

#### 2. **`charCodeAt(index)`**
   - Belirtilen indeksteki karakterin Unicode değerini döndürür.
   - Örnek: `'A'.charCodeAt(0)` // 65

#### 3. **`concat(string2, string3, ...)`**
   - String'leri birleştirir.
   - Örnek: `'Merhaba'.concat(' ', 'Dünya')` // "Merhaba Dünya"

#### 4. **`includes(substring, start)`**
   - String'in belirtilen alt stringi içerip içermediğini kontrol eder.
   - Örnek: `'Merhaba Dünya'.includes('Dünya')` // true

#### 5. **`endsWith(substring, length)`**
   - String'in belirtilen alt string ile bitip bitmediğini kontrol eder.
   - Örnek: `'Merhaba'.endsWith('ba')` // true

#### 6. **`indexOf(substring, start)`**
   - Alt stringin, string içinde ilk geçtiği yerin indeksini döndürür.
   - Örnek: `'Merhaba'.indexOf('e')` // 1

#### 7. **`lastIndexOf(substring, start)`**
   - Alt stringin, string içinde son geçtiği yerin indeksini döndürür.
   - Örnek: `'Merhaba Dünya'.lastIndexOf('a')` // 11

#### 8. **`match(regex)`**
   - String'i, belirtilen düzenli ifade (regex) ile eşleştirir ve eşleşmeleri bir dizi olarak döndürür.
   - Örnek: `'abc123'.match(/\d+/)` // ["123"]

#### 9. **`replace(searchValue, newValue)`**
   - String içinde belirli bir değeri yeni bir değerle değiştirir.
   - Örnek: `'Merhaba Dünya'.replace('Dünya', 'JavaScript')` // "Merhaba JavaScript"

#### 10. **`search(regex)`**
   - Belirtilen düzenli ifadeye (regex) uyan ilk değerin indeksini döndürür.
   - Örnek: `'abc123'.search(/\d/)` // 3

#### 11. **`slice(start, end)`**
   - String'in belirtilen aralıktaki bir kısmını döndürür.
   - Örnek: `'Merhaba'.slice(0, 4)` // "Merh"

#### 12. **`split(separator, limit)`**
   - String'i, belirli bir ayırıcıya göre böler ve bir dizi olarak döndürür.
   - Örnek: `'Merhaba Dünya'.split(' ')` // ["Merhaba", "Dünya"]

#### 13. **`startsWith(substring, start)`**
   - String'in belirtilen alt string ile başlayıp başlamadığını kontrol eder.
   - Örnek: `'Merhaba'.startsWith('Mer')` // true

#### 14. **`substring(start, end)`**
   - String'in belirtilen aralıktaki bir kısmını döndürür (slice'a benzer).
   - Örnek: `'Merhaba'.substring(1, 4)` // "erh"

#### 15. **`toLowerCase()`**
   - String'in tüm karakterlerini küçük harfe çevirir.
   - Örnek: `'MERHABA'.toLowerCase()` // "merhaba"

#### 16. **`toUpperCase()`**
   - String'in tüm karakterlerini büyük harfe çevirir.
   - Örnek: `'merhaba'.toUpperCase()` // "MERHABA"

#### 17. **`trim()`**
   - String'in başındaki ve sonundaki boşlukları kaldırır.
   - Örnek: `'  Merhaba  '.trim()` // "Merhaba"

#### 18. **`trimStart()` veya `trimLeft()`**
   - String'in başındaki boşlukları kaldırır.
   - Örnek: `'  Merhaba'.trimStart()` // "Merhaba"

#### 19. **`trimEnd()` veya `trimRight()`**
   - String'in sonundaki boşlukları kaldırır.
   - Örnek: `'Merhaba  '.trimEnd()` // "Merhaba"

#### 20. **`valueOf()`**
   - String nesnesinin ilkel (primitive) değerini döndürür.
   - Örnek: `'Merhaba'.valueOf()` // "Merhaba"

#### 21. **`padStart(targetLength, padString)`**
   - String'in başına, belirli bir uzunluğa ulaşana kadar belirtilen karakterleri ekler.
   - Örnek: `'5'.padStart(3, '0')` // "005"

#### 22. **`padEnd(targetLength, padString)`**
   - String'in sonuna, belirli bir uzunluğa ulaşana kadar belirtilen karakterleri ekler.
   - Örnek: `'5'.padEnd(3, '0')` // "500"

#### 23. **`repeat(count)`**
   - String'i belirtilen sayıda tekrarlar.
   - Örnek: `'Merhaba'.repeat(3)` // "MerhabaMerhabaMerhaba"

#### 24. **`localeCompare(compareString)`**
   - İki string'i, dil duyarlı olarak karşılaştırır.
   - Örnek: `'a'.localeCompare('b')` // -1 (a, b'den önce gelir)

#### 25. **`toString()`**
   - String nesnesini temsil eden bir string döndürür.
   - Örnek: `String(123).toString()` // "123"

Bu metotlar, JavaScript'te string manipülasyonları yapmak için yaygın olarak kullanılır ve birçok farklı senaryoda işlevsellik sağlarlar.