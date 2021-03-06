---
id: 5a24bbe0dba28a8d3cbd4c5d
title: 创建一个复杂的 JSX 元素
challengeType: 6
forumTopicId: 301382
---

# --description--

上一个挑战是 JSX 的一个简单示例，但 JSX 也可以表示更复杂的 HTML。

关于嵌套的 JSX，你需要知道的一件重要的事情，那就是它必须返回单个元素。

这个父元素将包裹所有其他级别的嵌套元素。

例如，几个作为兄弟元素而编写的JSX元素没有父元素包裹将不会被转换。

这里是一个示例：

**有效的 JSX：**

```jsx
<div>
  <p>Paragraph One</p>
  <p>Paragraph Two</p>
  <p>Paragraph Three</p>
</div>
```

**无效的 JSX：**

```jsx
<p>Paragraph One</p>
<p>Paragraph Two</p>
<p>Paragraph Three</p>
```

# --instructions--

定义一个新的常量`JSX`，渲染一个`div`，其中依次包含以下元素：

一个`h1`，一个`p`，一个包含三个`li`项的无序列表。你可以在每个元素中包含任何你想要的文本。

**注意：** 当像这样渲染多个元素时，你可以把它们都用圆括号括起来，但是这并不是必须的。还请注意，此挑战使用`div`标签把所有子元素包裹在里面。如果删除`div`，JSX 将不会编译这些元素。请记住这一点，因为当你在 React 组件中返回 JSX 元素时它也适用。

# --hints--

常量`JSX`应该返回一个`div`元素。

```js
assert(JSX.type === 'div');
```

`div`应该包含一个`p`标签作为第二个元素。

```js
assert(JSX.props.children[0].type === 'h1');
```

`div`应该包含一个`ul`标签作为第三个元素。

```js
assert(JSX.props.children[1].type === 'p');
```

`div`应该包含一个`h1`标签作为第一个元素。

```js
assert(JSX.props.children[2].type === 'ul');
```

`ul`应该包含三个`li`元素。

```js
assert(
  JSX.props.children
    .filter((ele) => ele.type === 'ul')[0]
    .props.children.filter((ele) => ele.type === 'li').length === 3
);
```

# --solutions--

