# CSS Guidelines

This document are my set of rules when writing CSS. Also worh mentioning [CSS Guidlines](https://cssguidelin.es/) which I highly recommend reading.

## Basics

One selector per line

```css
p,
li {}
```

Comments should always appear above what it describes and on a separate line (never behind a declaration)

```css
/* Module */
.box {}
```

Leave a space after colons

```css
color: #efefef;
```

Always use color shortcodes when possible:

```css
color: #000;
```

## Declaration order

It is a good practise to write CSS in some order. 
_Alternatively you can use a tool such as [css comb](http://csscomb.com/)._ 

```css
.selector {

  /* Positioning */
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;

  /* Box-model */
  display: flex;
  flex-direction: column;
  align-item: center;
  justify-content: space-between:;
  
  /* Of course you wouldn't want to try to float anything when using flexbox ;) */
  float: right;
  margin: 0;
  padding: 0;
  width: 100%;
  height: auto;
  border-box: content-box;

  /* Typography */
  font: normal 13px "Helvetica Neue", sans-serif;
  line-height: 1.5;
  color: #333;
  text-align: center;

  /* Visual */
  background-color: #f5f5f5;
  border: 1px solid #e5e5e5;
  border-radius: 3px;

  /* Misc */
  transform: skew(30deg, 20deg);
  transition: background-color .3s;
  opacity: 1;
}
```

### Pseudo elements

```css
selector::before, 
selector::after {
  content: '';
  ...
}
```

## Extra tips

- Never use `id`s for styling
- Never style a data attribute or class that is prefixed with `js-` (ex. `js-main-nav`)
- Never style `data` attributes. They are for data not styling.
- Stick with a naming convention for example [BEM](http://getbem.com/naming/)
