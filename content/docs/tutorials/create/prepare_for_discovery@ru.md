---
$title: Подготовка страницы к обнаружению и распространению
---

В некоторых случаях вам могут понадобиться версии одной и той же страницы, например новостной статьи, выполненные как с использованием разметки AMP, так и без нее. Подумайте над следующим вопросом: если Google Поиск находит версию страницы без разметки AMP, *как он узнает о существовании версии с разметкой AMP*?

## Связывание страниц тегом &lt;link>

Для решения этой проблемы мы добавляем в страницу информацию о ее другой версии (с разметкой AMP или без нее) в виде тегов `<link>` в разделе `<head>`.

Добавьте следующий код в страницу, не использующую AMP:

[sourcecode:html]
<link rel="amphtml" href="https://www.example.com/url/to/amp/document.html">
[/sourcecode]

В страницу AMP добавьте следующее:

[sourcecode:html]
<link rel="canonical" href="https://www.example.com/url/to/full/document.html">
[/sourcecode]

## Если существует только одна страница

Если у вас есть только одна страница, которая использует разметку AMP, в нее следует включить каноническую ссылку на саму себя:

[sourcecode:html]
<link rel="canonical" href="https://www.example.com/url/to/amp/document.html">
[/sourcecode]

<a class="go-button button" href="/ru/docs/tutorials/create/publish.html">Перейти к шагу 6</a>