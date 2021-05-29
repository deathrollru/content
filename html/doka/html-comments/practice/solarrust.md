---
tags:
  - practice
permalink: false
---

🛠 Комментарии часто используют, чтобы пометить начало какого-то крупного куска кода, пояснить его назначение. Поскольку комментарии внешне отличаются от остального кода — выделены серым цветом — то иногда гораздо удобнее _просканировать_ код, пробежаться глазами по этим самым комментариям и найти нужную часть, чем вчитываться в сам код.

Комментарий — твой лучший друг 🤝

🛠 Иногда для подключения чего-нибудь на страницу требуется скопировать-вставить блок кода, написанного не тобой. Чаще всего блок кода сопровождается комментариями. Всегда копируй весь код вместе с этими комментариями и вставляй его к себе в неизменном коде. Тебе же будет проще потом понять, что эта за странная конструкция и зачем она тут нужна.

Например, для подключения Яндекс.Метрики к сайту нужен такой код:

```html
<!-- Yandex.Metrika counter -->
<script>
  ;(function (d, w, c) {
    ;(w[c] = w[c] || []).push(function () {
      try {
        w.yaCounter64735912 = new Ya.Metrika({
          id: identification,
          clickmap: true,
          trackLinks: true,
          accurateTrackBounce: true,
        })
      } catch (e) {}
    })

    var n = d.getElementsByTagName("script")[0],
      s = d.createElement("script"),
      f = function () {
        n.parentNode.insertBefore(s, n)
      }
    s.async = true
    s.src = "https://mc.yandex.ru/metrika/watch.js"

    if (w.opera == "[object Opera]") {
      d.addEventListener("DOMContentLoaded", f, false)
    } else {
      f()
    }
  })(document, window, "yandex_metrika_callbacks")
</script>
<noscript
  ><div>
    <img
      src="https://mc.yandex.ru/watch/id"
      style="position:absolute; left:-9999px;"
      alt=""
    /></div
></noscript>
<!-- /Yandex.Metrika counter -->
```

Видишь, он начинается с комментария и комментарием заканчивается? Это удобно, визуально отделяет код метрики от остального кода. В дальнейшем тебе проще будет его найти.

🛠 Читая чужой код, обращай внимание на комментарии. Там могут скрываться важные детали и подсказки, которые помогут тебе понять, как этот код работает и почему именно так.

🛠 Комментарии делятся на строчные: когда вы просто написали небольшое сообщение — и блоковые: когда выделяется целый объект. В блоковых комментариях принято обозначать их начало и конец, например:

```html
<!-- это обычный срочный комментарий -->

<!-- ниже будут блоковые комментарии -->
<!-- header -->
<header class="header">
  <img src="logo.jpg" class="logo" />
</header>
<!-- /header -->

<!-- main -->
<main>
  <p class="text">
    Разработчики увидят раздел кода, который имеет общий смысл.
  </p>
</main>
<!-- END main -->
```

🛠 Комментарии видны в браузере в инструментах разработчика, поэтому в них стоит оставить только документацию, которая поможет работе с кодом. Планы, впечатления и мнения стоит оставить в недоступном для конечных пользователей месте.