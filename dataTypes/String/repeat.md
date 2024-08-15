## Javascript String Repeat Metodu Örnekleri:

`repeat()` metodu, bir string'i belirtilen sayıda tekrarlayarak yeni bir string döndürür.

**Sözdizimi:**
```javascript
string.repeat(count);
```

**Parametreler:**

* **count:** Tekrar sayısını belirten bir tam sayı. Negatif sayılar girilirse `RangeError` hatası verir. 

**Geri Dönüş Değeri:**

* Orijinal string'in belirtilen sayıda tekrarlanmasından oluşan yeni bir string.

**Örnekler:**

1. **Basit Tekrarlama:**
   ```javascript
   const str = "Merhaba ";
   const tekrarlananStr = str.repeat(3);
   console.log(tekrarlananStr); // Çıktı: Merhaba Merhaba Merhaba 
   ```
   > "Merhaba " string'i 3 kere tekrarlanarak yeni bir string oluşturulur.

2. **Boş String Tekrarlama:**
   ```javascript
   const boşStr = "";
   const tekrarlananBoşStr = boşStr.repeat(5);
   console.log(tekrarlananBoşStr); // Çıktı: 
   ```
   > Boş bir string kaç kere tekrarlanırsa tekrarlansın sonuç yine boş string olur.

3. **Sayı ile Tekrarlama:**
   ```javascript
   const sayıStr = "5";
   const tekrarlananSayıStr = sayıStr.repeat(4);
   console.log(tekrarlananSayıStr); // Çıktı: 5555
   ```
   > "5" string'i 4 kere tekrarlanarak "5555" string'ini oluşturur.

4. **Özel Karakter Tekrarlama:**
   ```javascript
   const karakter = "-";
   const tekrarlananKarakter = karakter.repeat(10);
   console.log(tekrarlananKarakter); // Çıktı: ----------
   ```
   > "-" karakteri 10 kere tekrarlanarak yeni bir string oluşturulur.

5. **Değişken Kullanarak Tekrarlama:**
   ```javascript
   const tekrarSayısı = 7;
   const kelime = "JS ";
   const tekrarlananKelime = kelime.repeat(tekrarSayısı);
   console.log(tekrarlananKelime); // Çıktı: JS JS JS JS JS JS JS 
   ```
   > "JS " string'i "tekrarSayısı" değişkeninin değeri kadar (7) tekrarlanır.

6. **Satır Atlama Ekleme:**
   ```javascript
   const satır = "Satır 1\n";
   const çokluSatır = satır.repeat(3);
   console.log(çokluSatır); 
   /* Çıktı: 
   Satır 1
   Satır 1
   Satır 1
   */
   ```
   > "\n" kaçış dizisi kullanılarak her tekrarda yeni satıra geçilir.

7. **Döngü İçinde Kullanım:**
   ```javascript
   let yıldızlar = "";
   for (let i = 1; i <= 5; i++) {
     yıldızlar += "*".repeat(i) + "\n"; 
   }
   console.log(yıldızlar);
   /* Çıktı: 
   *
   **
   ***
   ****
   *****
   */
   ```
   > Döngü içinde her adımda "*" karakteri artan sayıda tekrarlanarak piramit şekli oluşturulur.

8. **Koşula Bağlı Tekrarlama:**
   ```javascript
   const durum = true;
   const metin = durum ? "Doğru ".repeat(2) : "Yanlış";
   console.log(metin); // Çıktı: Doğru Doğru 
   ```
   > "durum" değişkenine göre farklı string'ler tekrarlanır.

9. **Fonksiyon İçinde Kullanım:**
   ```javascript
   function tekrarla(str, count) {
     return str.repeat(count);
   }
   const sonuç = tekrarla("ABC", 4);
   console.log(sonuç); // Çıktı: ABCABCABCABC
   ```
   > `tekrarla()` fonksiyonu string ve tekrar sayısını parametre olarak alıp tekrarlanan string'i döndürür.

10. **Hata Durumu:**
    ```javascript
    const hataStr = "Hata!";
    const tekrarlananHataStr = hataStr.repeat(-2); // RangeError: Invalid count value
    console.log(tekrarlananHataStr); 
    ```
    > Negatif tekrar sayısı `RangeError` hatasına sebep olur.

Bu örnekler, `repeat()` metodunun string'leri nasıl tekrarlayabileceğinizi ve farklı senaryolarda nasıl kullanabileceğinizi göstermektedir. 
