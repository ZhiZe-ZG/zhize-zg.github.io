---
title: "Using Mermaid in GitHub Pages"
date: 2024-04-16 15:43:45 +0800
category: Tech-Note/Personal-Website
tags: Jekyll GitHub-Pages Mermaid Front-Matter Minimal-Mistakes Liquid
header:
  teaser: http://mermaid.js.org/mermaid-logo.svg
mermaid: true
---

Mermaid is a markup language for describing diagrams. It is generally used embedded in HTML or Markdown. There are some Jekyll plugins that provide Mermaid support. But actually, you don’t need these plugins to use Mermaid with GitHub Pages.

## Theory and Practice

Mermaid is a JavaScript module. You can load it in HTML. Then it will automatically parse the `pre` tags whose `class` attribute is `mermaid` in the HTML page and render them into SVG images for display.

So what we actually have to do is two things:

1. Add a statement to load the mermaid script in the HTML page.
1. Create `pre` tags (with the `class="mermaid"`) and write the Mermaid code in it.

For the first thing, you just need add this to your Markdown or HTML:

```html
<!-- Mermaid Support -->
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({
    startOnLoad: true,
    theme: 'dark'
  });
</script>
```

For the second step, here is an example:

```html
<pre class="mermaid">
flowchart TD
    QLogic[Can the things be logically grouped?]
    QDate[Are they grouped by date?]
    UPages[Use pages]
    UPosts[Use Posts]
    UCollection[Use a collections]

    QLogic -- No --> UPages
    QLogic -- Yes --> QDate
    QDate -- No --> UCollection
    QDate -- Yes --> UPosts
</pre>
```

If everything is ok, it will shows:

<pre class="mermaid">
flowchart TD
    QLogic[Can the things be logically grouped?]
    QDate[Are they grouped by date?]
    UPages[Use pages]
    UPosts[Use Posts]
    UCollection[Use a collections]

    QLogic -- No --> UPages
    QLogic -- Yes --> QDate
    QDate -- No --> UCollection
    QDate -- Yes --> UPosts
</pre>

## Set Up Script Loading in Layout

Adding a piece of JavaScript loading code to every page that needs to be rendered by Mermaid will make the page look very messy. Therefore, you can add this code directly to Jekyll's layout.

At the same time, in order to prevent the script from being loaded on pages that do not require Mermaid and slowing down page rendering, we also need a variable in Front Matter to control whether the Mermaid script is loaded. Here is my solution:

Generally I use `single` as the layout for posts. So the first step is to go to the Minimal Mistakes GitHub repository and copy the layout into our `_layout`. This will overwrite the [original `single` layout](https://github.com/mmistakes/minimal-mistakes/blob/master/_layouts/single.html).

The second step is to add the following code at the front of our `single.html` (before the text content):

{% raw %}

```liquid
{% if page.mermaid %}
<!-- Mermaid Support -->
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({
    startOnLoad: true,
    theme: 'dark'
  });
</script>
{% endif %}
```

{% endraw %}

The `if` determines whether to add the content included in `if` based on the value of the `mermaid` variable in the page's Front Matter. Inside the `if` statement is the code to load Mermaid. This is a piece of JavaScript code embedded in HTML that will go to Mermaid's distribution website to download the Mermaid script and run it on the current page. You can also modify this if you can read JavaScript.

On the post page, add `mermaid=ture` to enable rendering of `<pre class="mermaid">`. For example:

```yaml
---
title: "Using Mermaid in GitHub Pages"
date: 2024-04-16 15:43:45 +0800
category: Tech-Note/Personal-Website
tags: Jekyll GitHub-Pages Mermaid Front-Matter Minimal-Mistakes Liquid
header:
  teaser: http://mermaid.js.org/mermaid-logo.svg
mermaid: true
---
```
