# ☺ Değişkenler ve Veri Türleri

Kotlin programlama dilinde değişkenler ve veri türleri kullanımı oldukça basittir. İşte Kotlin'de değişkenlerin tanımlanması ve bazı yaygın veri türlerinin kullanımı hakkında temel bilgiler:

## **Değişken Tanımlama**

Kotlin'de bir değişken tanımlamak için `var` veya `val` anahtar kelimelerini kullanabilirsiniz. `var` ile tanımlanan değişkenler değiştirilebilirken, `val` ile tanımlanan değişkenler değiştirilemez (read-only) ve sadece bir kez değer atanabilir.

<pre class="language-kotlin" data-overflow="wrap" data-line-numbers><code class="lang-kotlin">var testChange: Int = 5 // Replaceable
<strong>val testNotChange: String = "Merhaba" // Cannot be changed
</strong></code></pre>

## **Veri Türleri**

Kotlin 'de yaygın veri türleri şunlardır:

* `Int`: Tam sayıları temsil eder. Maksimum değer 2,147,483,647'dir.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
var sayi: Int = 10
var sayi = 10
```
{% endcode %}

* `Double`: Ondalık sayıları temsil eder. Yaklaşık maksimum değer 1.7976931348623157 x 10^308'dir.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
var sayi: Double = 10.0
var sayi = 10.0
```
{% endcode %}

* `Float`: İkili ondalık sayıları temsil eder. Yaklaşık maksimum değer 3.40282347 x 10^38'dir.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
var sayi: Float = 10.0f
var sayi = 10.0f
```
{% endcode %}

* `String`: Metin verilerini temsil eder.

{% code overflow="wrap" lineNumbers="true" fullWidth="false" %}
```kotlin
val helloWorld: String = "Hello World"
val helloWorld = "Hello World"
```
{% endcode %}

* `Boolean`: Doğru veya Yanlış değerlerini temsil eder.

```kotlin
val isLogin: Boolean = true
val isLogin = false
```

* `List`: Listeleri temsil eder.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
// Creating a list of integers
val numbers = listOf(1, 2, 3, 4, 5)

// Accessing elements in a list
val firstNumber = numbers[0] // Retrieves the first element (1)

// Iterating through a list
for (number in numbers) {
    println(number)
}

// Adding elements to a mutable list
val mutableNumbers = mutableListOf(1, 2, 3)
mutableNumbers.add(4)
mutableNumbers.add(5)

// Removing elements from a mutable list
mutableNumbers.removeAt(0) // Removes the first element (1)

```
{% endcode %}

* `Map`: Sözlükleri (anahtar-değer çiftleri) temsil eder

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
// Creating a map of strings to integers
val personAge = mapOf("Alice" to 25, "Bob" to 30, "Charlie" to 35)

// Accessing values in a map using keys
val aliceAge = personAge["Alice"] // Retrieves the value associated with the key "Alice" (25)

// Iterating through a map
for ((name, age) in personAge) {
    println("$name is $age years old")
}

// Adding and updating values in a mutable map
val mutablePersonAge = mutableMapOf("Alice" to 25, "Bob" to 30)
mutablePersonAge["Charlie"] = 35 // Adds a new key-value pair
mutablePersonAge["Alice"] = 26 // Updates the value for the key "Alice"

```
{% endcode %}

* `Set`: Küme verilerini temsil eder.

{% code overflow="wrap" lineNumbers="true" %}
```kotlin
// Creating a set of integers
val uniqueNumbers = setOf(1, 2, 3, 4, 5, 5) // Note that duplicate values are automatically removed

// Checking if an element exists in a set
val containsThree = uniqueNumbers.contains(3) // Returns true

// Iterating through a set
for (number in uniqueNumbers) {
    println(number)
}

// Adding and removing elements from a mutable set
val mutableUniqueNumbers = mutableSetOf(1, 2, 3)
mutableUniqueNumbers.add(4)
mutableUniqueNumbers.remove(2)

```
{% endcode %}
