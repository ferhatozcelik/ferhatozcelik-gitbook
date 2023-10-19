# 📎 Android Activity Sınıfı

## Activity Nedir?

Activity sınıfı bir android uygulamasının en önemli parçalarından birisidir. Basitçe anlatmak gerekirse android uygulamasındaki bir ekranı temsil eder. Bir Activity, kullanıcıyla etkileşimde bulunmanıza, kullanıcı arayüzünü oluşturmanıza ve yönetmenize olanak tanır.

> Activity sınıfı, bir Android uygulamasının önemli bir bileşeni olup, activity lerin nasıl başlatıldığı ve bir araya getirildiği, platformun uygulama modelinin temel bir parçasını oluşturur. Diğer programlama paradigmalarının aksine, Android sistemi uygulamaları bir "main()" yöntemi ile başlatmak yerine, yaşam döngüsünün(life cycle) belirli aşamalarına karşılık gelen belirli callback methodlarını çağırarak bir Activity örneğinde kodu başlatır.
>
> — Kaynak\*\*:\*\* [https://developer.android.com/guide/components/activities/intro-activities](https://developer.android.com/guide/components/activities/intro-activities)

Bir activity oluşturduktan sonra, bu activity i kullanabilmek için AndroidManifest.xml dosyanıza eklemeniz gerekmektedir.

{% code fullWidth="false" %}
```xml
<manifest ... >
  <application ... >
      <activity android:name=".YourActivity" />
      ...
  </application ... >
  ...
</manifest >
```
{% endcode %}

***

### Activityler için Intent Filters Tanımlama

İntent'ler, Android uygulamalarında Activity'leri başlatmak ve uygulama bileşenleri arasında iletişim kurmak için kullanılır. Bu sayede kullanıcı arayüzü ekranları arasında geçiş yapabilir ve diğer uygulamalarla etkileşime girebilirsiniz

Intent Filter'lar, bir Activity'nin hangi tür Intent'lere (intention, niyet) yanıt vereceğini belirtmek için kullanılır. Bu şekilde, belirli eylemleri veya veri tiplerini işlemek için o Activity'yi kullanılabilir hale getirebilirsiniz. Bu, Android uygulamalarınızın diğer bileşenlerle ve uygulamalarla nasıl etkileşime gireceğini ve hangi tür Intent'lere tepki vereceğini kontrol etmenizi sağlar.

```xml
<activity android:name=".YourActivity" android:icon="@drawable/app_icon">
    <intent-filter>
        <action android:name="android.intent.action.SEND" />
        <category android:name="android.intent.category.DEFAULT" />
        <data android:mimeType="text/plain" />
    </intent-filter>
</activity>
```

{% hint style="info" %}
_**\<action>**_ elementi ile bu activity'nin veri göndereceğini belirtiyoruz.

_**\<category>**_ elementi ile activity'nin launch (başlatma) istekleri alabileceğini belirtiyoruz.

_**\<data>**_ elementi ile bu activity'nin hangi türde veri gönderebileceğini belirtiyoruz.
{% endhint %}

Diğer uygulamaların erişimini istemediğiniz Activity'ler için Intent Filter tanımlamamak daha güvenli bir yaklaşımdır. Bu Activity'leri yalnızca kendi uygulamanız içinden Explicit Intent'ler kullanarak başlatabilirsiniz. Bu şekilde, uygulamanızın güvenliği daha iyi korunur ve istenmeyen erişimler engellenmiş olur.

Aşağıdaki kod bloğu bir activityi intent ile nasıl başlatabileceğinize bir örnektir.

```kotlin
val sendIntent = Intent().apply {
    action = Intent.ACTION_SEND
    type = "text/plain"
    putExtra(Intent.EXTRA_TEXT, textMessage)
}
startActivity(sendIntent)
```

***

### İzinlerin Tanımlanması

Activity'ler için izinler tanımlamak mümkündür. İzinler, uygulamanın belirli kaynaklara veya işlevlere erişimini kontrol etmek için kullanılır. Herhangi bir Activity'nin belirli izinlere sahip olması, o Activity'nin yalnızca bu izinlere sahip olan uygulamalar veya kullanıcılar tarafından erişilmesine izin verir.

{% hint style="info" %}
Bir ana Activity, aynı izinlere sahip olmadıkça bir alt Activity'i başlatamaz.
{% endhint %}

Bir uygulama, _**`SHARE_POST`**_ iznine sahip bir Activity'i başlatabilmek için kendi manifest dosyasında ilgili izne sahip olmalıdır. Bu, izinlerin uygulamalar arasında etkileşimi ve güvenliği kontrol etmek için önemli bir rol oynar.&#x20;

_**Örnek uygulama:**_

```xml
<manifest>
<activity android:name="...."
   android:permission=”com.google.socialapp.permission.SHARE_POST”

/>
```

_**Bizim uygulamamız:**_

```xml
<manifest>
   <uses-permission android:name="com.google.socialapp.permission.SHARE_POST" />
</manifest>
```

