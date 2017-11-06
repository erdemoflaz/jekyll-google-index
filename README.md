## Jekyll Blogların Google İndexini Arttırma

Wordpress ve blogger da olduğu gibi sizde kendi jekyll bloglarınızda kategori ve etiket sayfalarını generate edebilirsiniz

[DEMO](https://erdemoflaz.com/)

---

## Kullanım

### Categories/Tags sayfaları için

Öncelikle eğer yoksa `_plugins` klasörü oluşturup, bu klasörün altına `categories.rb` ve `tags.rb` dosyalarını oluşturun



### Categories/Tags layouts

plugins klasörünün altına oluşturduğumuz dosyalardan sonra layout klasörünün altına `categories.html` ve `tags.html` dosyalarını da oluşturun.



Oluşturduğumuz **Category Layout:** dosyasına şu kodları ekleyin

		{% for post in site.categories[page.category] %}
			burada postlarınızın özeti, thumbnail'ı felan olabilir
		{% endfor %}

Ardından,

Oluiturduğumuz **Tag Layout:** dosyasına da  şu kodları ekleyin

		{% for post in site.tags[page.tag] %}
			burada postlarınızın özeti, thumbnail'ı felan olabilir
		{% endfor %}


## Önemli Not:

Bu işlemleri uygulayıp, localinizde çalıitırabilirsiniz. Herşey tıkır tıkır çalışacaktır fakat, asıl önemli olan nokta ise dosyaları pushlayıp site adresinize çıkardığınızda ise github'ın aldığı güvenlik önlemlerine takılacağınız için kodlar çalışmayacak.

Bunun için de `_site` klasörü altına cachelenen categories ve tags klasörlerini ana dizine çıkartıp öyle pushlarsanız yaptıklarınız çalışmaya başlayacaktır.
