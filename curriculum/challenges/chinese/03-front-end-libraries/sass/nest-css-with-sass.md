---
id: 587d7dbd367417b2b2512bb5
title: 用 Sass 嵌套 CSS
challengeType: 0
forumTopicId: 301457
---

# --description--

Sass 允许 CSS 规则的`嵌套`，这在写样式表的时候会很有用。

在 CSS 里，每个元素的样式都需要写在独立的代码块中，如下所示：

```scss
nav {
  background-color: red;
}

nav ul {
  list-style: none;
}

nav ul li {
  display: inline-block;
}
```

对于一个大型项目，CSS 规则会很复杂。这时，引入`嵌套`功能（即在对应的父元素中写子元素的样式）可以有效地简化代码：

```scss
nav {
  background-color: red;

  ul {
    list-style: none;

    li {
      display: inline-block;
    }
  }
}

```

# --instructions--

根据上面关于嵌套的例子，来简化<code>.blog-post<code>中两个子元素的 CSS 代码。出于测试目的，<code>h1</code>应该出现在<code>p</code>元素之前。</code></code>

# --hints--

你应重新组织 CSS 规则，以便`h1`和`p`嵌套在`.blog-post`父元素中。

```js
assert(
  code.match(
    /\.blog-post\s*?{\s*?h1\s*?{\s*?text-align:\s*?center;\s*?color:\s*?blue;\s*?}\s*?p\s*?{\s*?font-size:\s*?20px;\s*?}\s*?}/gi
  )
);
```

# --solutions--

