# 😃 Fonksiyonlar ve Metotlar

Kotlin'de fonksiyonlar ve metotlar (sınıf içinde tanımlanan fonksiyonlar) tanımlamak oldukça benzerdir. İşte Kotlin'de fonksiyonlar ve metotlar oluşturmanın temel özellikleri:

**Fonksiyon Tanımlama**

Kotlin'de fonksiyonlar `fun` anahtar kelimesi ile tanımlanır. Bir fonksiyonun adı, parametreleri ve dönüş türü belirtilmelidir.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
fun topla(a: Int, b: Int): Int {
    return a + b
}
```
{% endcode %}

Bu örnekte, `topla` adında bir fonksiyon, iki tamsayı parametre alır ve bir tamsayı değer döndürür.

**Metot Tanımlama**

Kotlin'de sınıfların içinde tanımlanan fonksiyonlara metot denir. Metotlar da `fun` anahtar kelimesiyle tanımlanır.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
class HesapMakinesi {
    fun topla(a: Int, b: Int): Int {
        return a + b
    }
}
```
{% endcode %}

Bu örnekte, `HesapMakinesi` adında bir sınıf tanımlanmış ve bu sınıfın içinde `topla` adında bir metot tanımlanmıştır.

**Fonksiyonları Çağırma**

Tanımlanan bir fonksiyonu çağırmak için sadece fonksiyon adını ve gerekli parametreleri kullanmanız yeterlidir:

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
val sonuc = topla(5, 3)
println("Toplam: $sonuc")

val hesapMakinesi = HesapMakinesi()
val sonuc = hesapMakinesi.topla(5, 3)
println("Toplam: $sonuc")
```
{% endcode %}

Kotlin'de fonksiyonlar ve metotlar oldukça esnek ve güçlüdür. Parametrelerin ve dönüş değerlerinin türleri belirli değilse (`Any` gibi), Kotlin'de otomatik olarak tür çıkarımı yapılır. Ayrıca, fonksiyonlar yüksek siparişli fonksiyonlar olarak kullanılabilir ve lambda ifadeleri gibi işlevsel programlama özelliklerini destekler.
