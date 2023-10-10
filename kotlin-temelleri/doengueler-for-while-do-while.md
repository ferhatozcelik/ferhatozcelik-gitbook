# 😂 Döngüler (for, while, do-while)

Kotlin, döngüler için çeşitli seçenekler sunar: `for`, `while` ve `do-while`. Bu döngülerle tekrarlayan işlemler gerçekleştirebilirsiniz.

## FOR

`for` döngüsü, bir dizi veya başka bir veri koleksiyonu üzerinde dolaşmak için kullanılır.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
val numbers = listOf(1, 2, 3, 4, 5)
for (number in numbers) {
    println(number)
}
```
{% endcode %}

## WHILE

`while` döngüsü, belirli bir koşul doğru olduğu sürece işlemleri tekrarlamak için kullanılır.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
var i = 0
while (i < 5) {
    println(i)
    i++
}
```
{% endcode %}

## DO-WHILE

`do-while` döngüsü, döngünün içeriğini en az bir kez çalıştırmak için kullanılır, ardından koşul kontrol edilir.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
var x = 0
do {
    println("Bu en az bir kez çalışacak")
} while (x > 0)

```
{% endcode %}

Kotlin 'de döngülerin çalışma mantığı, diğer programlama dilleriyle benzerdir. Döngüleri kullanırken, döngü koşullarını ve döngü içindeki işlemleri doğru bir şekilde ayarlamak önemlidir. Ayrıca sonsuz döngülere dikkat etmek ve döngüden çıkış koşullarını sağlamak gereklidir.
