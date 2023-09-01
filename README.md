# Descendant-selector
## Another variant of Css selector is descendant selector(Css selectorun başka bir çeşidi descendant selector)
- Soydan gelen seçicidir. Bir boşlukla kullanılır. Diyelim ki; sayfamda çok fazla __a href__ etiketi mevcut. Ben içlerinden bazılarına stil vereceğim. O zaman __descendant selector__ yardımıyla seçerek kullanabilirim.
```html
<main>
        <h1>Popular Posts</h1>
        <section class="post">
            <span>Posted by <a href="#213adas">/u/not_funny</a></span>
            <h2>Lol look at this hilarious name <span class="tag">funny</span></h2>
            <button>+Vote</button>
            <hr>
        </section>
        <section class="post">
            <span>Posted by <a href="#345adas">/u/gooner4lyfe</a></span>
            <h2>Happy birthday to the strongest defender/bodyguard in the Prem! <span class="tag">gunners </span></h2>
            <button>+Vote</button>
            <hr>
        </section>
</main>
<footer>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="https://www.google.com">Google</a></li>
            </ul>
        </nav>
        <a href="#licence">Content is available under these licence</a>
</footer>
```
- __main__ kısmında bulunan "a" etiketlerine stil vereceğiz. __footer__ kısmındaki etiketler ise değişmeyecek.
---
```css
span a{
       color:red;
}
```

- __span a:__ span soyundan gelen a etiketini selector olarak kullanır. Bir boşluk ile selector oluşturulur.
- __color:__ Sadece _/u/not_funny & /u/gooner4lyfe_ rengini kırmızı yapar. Yalnız bu 2 etikete stil verir.
- Sadece __main__ içindeki a etiketlerine stil vermek istediğimiz için bu şekilde kullanabiliriz.
- __main__ içindeki "a" etiketleri __span__ içinde yazıldığı için böyle bir kullanım mümkün.
---
- Aynı işlemi sectiona class tanımlaması yaparak da kullanabilirim. Kodumda hali hazırda sectionlar için __post__ adında class tanımlaması mevcut. Şimdi bu classı descendant selector ile beraber kullanalım.
```css
.post a{
       color:red;
}
```
- __.post a:__ class selectorları "." yardımıyla kullanıyorduk. O sebeple "." + "class ismi" dedikten sonra bir boşluk & soydan gelen etiket "a" yazılarak descendant selector oluşturulur.
- __color:__ Sadece _/u/not_funny & /u/gooner4lyfe_ rengini kırmızı yapar. Yalnız bu 2 etikete stil verir.
---
- Her iki kullanım da aynı işlemi yapar. Fakat class yardımıyla descendant oluşturmak daha seçici bir kullanım şeklidir.
- Her düğmeye(__button__) bir class ya da her bağlantı etiketine(__a href__) bir class vermek yerine; ana elemana(__section__) class vermek ve bunu kullanmak daha mantıklıdır.
  
  _İyi kodlamalar.._





