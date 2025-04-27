---
layout: article
title: Как добавлять и вносить правки
tags: FAQ
aside:
  toc: true
---

## Как добавлять заметки и вносить правки

Главное помнить: исходники в `Markdown` и наш сайт автоматически подцепляет и <!--more--> форматирует их за счёт [Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll). 

Для того чтобы править, например, эту страницу, попробуйте найти небольшую пиктограмму "Edit on Github" рядом с заголовком, и перейти на исходный код в репозитории.

Внимание, следующий по странице объект - не рекурсия, а фото экрана этой же страницы.
{:.warning}

![1]({{ site.baseurl }}/posts_images/2025-04-27_01.png){: width="500" }

Редактирование осуществляется c помошью отправки Merge запроса, см. инструкции для генератора [Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll).

### Тема оформления

Сайт работает на `dark` теме [TeXt-theme](https://kitian616.github.io/jekyll-TeXt-theme/docs/en/writing-posts). Много что в ней изменяемо, шлите предложения.

## Конвенции

### Записи

Файлы должны иметь вид `YYYY-MM-DD-lower-train-case.md`, это требуется для чтения даты при генерировании.

Читайте более подробно в [Writing Posts](https://kitian616.github.io/jekyll-TeXt-theme/docs/en/writing-posts) и в [adding content](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll).

### Файлы (например картинки)

* Используйте [Pixlr](https://pixlr.com/editor/) или любой другой онлайн-редактор для коррекций больших размеров изображений
* Используйте [TinyPng](https://tinypng.com/) или любой другой компрессор для улучшения степени сжатия файлов
* Файлы должны храниться в папке `src/posts_images` и иметь вид `YYYY-MM-DD_snake_case.ext`
* В Markdown должны иметь [site.baseurl](https://mademistakes.com/mastering-jekyll/site-url-baseurl/) в адресе, перед `/posts_images/`, например:

```
{% raw %}![Иллюстрация №1]({{ site.baseurl }}/posts_images/2025-04-27_01.png){: width="500" }{% endraw %}
```

* Да, Jekyll поддерживает аттрибуты СSS для изображений, наподобие `{: width="500" }` в примере выше

### Уточнение

На самом деле без разницы `snake_case` или `Train-case` главное сохраняйте `YYYY-MM-DD` в начале файлов. 

## Локальная копия

Для правок и новых страниц можно склонировать весь репозиторий и затем править его локально, на порту 4000, используя `bundle exec jekyll serve` как разъясняется в [примере quick start](https://kitian616.github.io/jekyll-TeXt-theme/docs/en/quick-start) 

Вам не требуется локальная копия чтобы создавать новые заметки или вносить правки
{:.warning}






Это не самый элегантный но наиболее простой на данный момент способ всем вносить правки.

Отправляйте PR-ы.

Новые страницы можно добавлять по образу и подобию в `src/_posts/`.

