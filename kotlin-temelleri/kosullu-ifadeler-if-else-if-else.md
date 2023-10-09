# 🤩 Koşullu İfadeler (if, else if, else)

Koşullu ifadeler (if, else if, else), programların belirli şartları değerlendirmesine ve buna göre farklı kod bloklarını çalıştırmasına olanak tanır. Bu ifadeler, programların akışını kontrol etmek için kullanılır ve belirli koşulların karşılanıp karşılanmadığını kontrol ederler. İşte koşullu ifadelerin kullanımıyla ilgili temel bilgiler:

## IF

if ifadesi, bir koşulu değerlendirir ve bu koşul doğru (true) ise belirtilen kod bloğunu çalıştırır. Aksi takdirde, kod bloğu atlanır. if ifadesi her zaman kullanılır ve birçok koşullu kontrol yapısının temelini oluşturur.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
val sayi = 10

if (sayi > 5) {
    println("Sayı 5'ten büyük.")
}
```
{% endcode %}

## ELSE IF

else if ifadesi, bir önceki ifadenin koşulu yanlışsa başka bir koşulu değerlendirir. Birden fazla koşulu kontrol etmek için kullanılır. Yine, sadece bir koşul doğruysa en yakın uygun kod bloğu çalıştırılır.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
val puan = 75

if (puan >= 90) {
    println("A aldınız.")
} else if (puan >= 80) {
    println("B aldınız.")
} else if (puan >= 70) {
    println("C aldınız.")
} else {
    println("Başarısız oldunuz.")
}
```
{% endcode %}

## ELSE&#x20;

else ifadesi, tüm önceki koşullar yanlışsa çalıştırılacak kod bloğunu belirtir. Yani hiçbir önceki koşul doğru değilse bu kod bloğu çalışır.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
val sayi = 3

if (sayi > 5) {
    println("Sayı 5'ten büyük.")
} else {
    println("Sayı 5'ten küçük veya eşit.")
}
```
{% endcode %}

Koşullu ifadeler, programların farklı durumları ele almasına ve kullanıcı girdilerine veya diğer faktörlere göre farklı davranışlar sergilemesine olanak tanır. İf, else if ve else ifadeleri kombinasyonlarını kullanarak daha karmaşık koşullu kontroller oluşturabilirsiniz.
