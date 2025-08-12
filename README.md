## HL10N(only 423b)
[中文文档](https://github.com/Love-Kogasa/hl10n)  
Complete your l10n in the same HTML  
**This library is only suitable for small projects. For complex requirements, please use other l10n or i18n libraries**

## Install
HL10N support browser only.
```html
<link rel="stylesheet" href="lang.css">
<!-- 隐藏lang元素，单独整一个css是因为我有一个习惯(，在前面先加载js -->
<link rel="stylesheet" href="l18n.min.js">
```
## Usage
```html
<!-- ... -->
<div>
  Hello <i>World</i>
  <!-- Use wildcards -->
  <lang zh*>
    你好，<b>世界</b>
  </lang>
  <!-- Wildcards are not used -->
  <lang en-US>
    Hi <s>the f**k</s> World.
  </lang>
</div>
<!-- ... -->
<script>
  l10n.renderAll()
</script>
```

## API
* l10n.renderAll( lang? )  
Render the entire page. "lang" is the language code of the target language or a special identifier of the "lang" tag. When the "lang" parameter is not passed, it defaults to the language code of the browser language  
* l10n.render( node, lang? )  
node represents the element to be rendered/element node, and the lang parameter is the same as above. These two methods will modify the page html, and special processing of the modified id element may be required