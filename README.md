# my-js-jquery-tips

1. [Load more list](#load-more-list)

### Load more list:

```html
<ul id="list">
    <li>One</li>
    <li>Two</li>
    <li>Three</li>
    <li>Four</li>
    <li>Five</li>
    <li>Six</li>
    <li>Seven</li>
</ul>
<div id="loadMore">Load more</div>
```

```js
var size_li = $("#list li").size();
x = 5;
$('#list li:lt('+x+')').show();
$('#loadMore').click(function () {
    x = (x+5 <= size_li) ? x+5 : size_li;
    $('#list li:lt('+x+')').show();
});
```
