# <h1 align="center"> Numpy Kütüphanesi Kullanarak Doğrusal Regresyon Uygulaması </h1>

---
<h3 align=center>(Linear Regression)</h3>

---

Makine öğrenmesine giriş seviyesindeki ilk adımınız **doğrusal regresyon** olabilir. **Regresyon** Türkçeye **bağlanım** olarak çevrilmiştir. Ancak genellikle regresyon kullanıldığı için bu çalışmada bu şekilde kullanmaya devam edeceğim. Matematiksel olarak kolay anlaşılır ve istatistiksel temelli bu model ile günlük hayatta bir çok konuda tahminleme yapma imkannı bulursunuz.

---

***Eğilim ve yönelimler, satış tahminleme, sigorta risk analizleri sık kullanıldıkları alanlardır.***

---

Elinizdeki en basitinden iki değişkenli verinin bir değişkeninin değerini diğerine bağlı olarak tahmin edebilirsiniz. Tahmin etmek için kullandığınız değişken **bağımsız**, tahmin etmek istediğiniz değişken ise **bağımlı** değişkendir. Bu tahminlemenin mümkün olduğu koşullarda doğrusal regresyon kullanabilirsiniz. 

* Ancak unutmamalı ki bağımlı ve bağımsız değişkenler nicel olmalıdır. Bağılmı değişkenin dağılımı her bağımsız değişken değeri için normal dağılıma sahip olması beklenir. Aralarındaki ilişki de doğrusal olmalıdır. Bu varsayımların bazıları sağlanmadığında farklı regresyon teknikleri uygulanabilir. 


* Tahmin etmek istediğiniz bağımlı değişkeni öngören birden fazla da bağımsız değişkeniniz olabilir. Burada doğrusal denklemin katsayıları tahmin edilerek analiz gerçekleştirirsiniz. 

* Tahminleme yaparken bir maliyet fonksiyonu tanımlanır ve bunu minimize ederek en iyi tahminleme yapılmaya çalışılır. Aşağıdaki temsili grafikten de anlayacağınız gibi maliyet fonksiyonu minimize edilirken doğrusal regresyon veri dağılımına fit eder.

![doğrusal regresyon](https://miro.medium.com/max/2400/1*AsfV2NelG1Ta5F-0kr727w.gif)

---

### Bu çalışmada da tam olarak böyle bir örneği adım adım gerçekleştireceğiz.
:dizzy_face: **Google Colab Not Defterinde Aç**  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ayyucekizrak/DogrusalRegresyonUygulamasi/blob/master/Doğrusal%20Regresyon%20Çalışma%20Dosyası.ipynb) 

**Çalışma için seçtiğimiz veri ve problem:** Doğrusal regresyon örneklemesinde çok kullanılan bir veri kümesini kullanacağız. Gıda taşımacılığı yapan bir kamyonun kâr kestirimini yapmaya çalışacağız. 

* İki sütundan oluşan bir veri kümemiz var ve ilk sütun şehirlerin popülasyonu hakkında bilgileri barındırırken ikinci sütun kamyonun kâr bilgisini barındırmaktadır. Bağımlı değişkenimiz bu kâr bilgisi olacak yani bunu doğrusal regresyonla bulmak istiyoruz. 

<h4 align=center> Hadi başlayalım!!!

![](https://media.giphy.com/media/liouol4vPRdDO/giphy.gif) </h4>

