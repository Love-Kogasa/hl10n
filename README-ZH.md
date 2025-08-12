## HL10N(仅402b)
在同一份HTML中完成你的l10n  
**本库仅适于小型项目，对于复杂的需求请使用其他的l10n或i18n库**

## Install
HL10N 仅支持浏览器环境
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
  <!-- 使用通配符 -->
  <lang zh*>
    你好，<b>世界</b>
  </lang>
  <!-- 通配符不使用 -->
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
渲染整页，lang为目标语言的语言代码或lang标签的特殊标识，当不传递lang参数时默认为浏览器语言语言代码  
* l10n.render( node, lang? )  
node为要渲染的元素/元素节点，lang参数同上，这两种方法会对页面html进行变动，可能需要对变动后的id元素进行特殊处理