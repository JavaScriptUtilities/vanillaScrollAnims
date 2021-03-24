# Vanilla ScrollAnims

Add animations to a webpage, triggered when scrolling

## How to install

First, load css/vanilla-scrollanims.css & js/vanilla-scrollanims.js in your webpage.

Then, when DOM is ready, start the plugin :

```js
// Find elements
var scrollItems = document.querySelectorAll('.will-scrollanim');
// Trigger plugin
var scrollAnim = new dkJSUScrollAnims(scrollItems, {});
```

## How to use

### Add a 500ms delay before trigger

```html
<img class="has-scrollanim" data-delay="500" src="images/image-1.jpg" alt="" />
```

### Wait until the top of an element is at least 100px above the bottom of the screen

```html
<img class="has-scrollanim" data-offset="-100" src="images/image-1.jpg" alt="" />
```

### Trigger on children, with a delay of 100ms between each call

```html
<div class="has-scrollanim" data-usechildren="1" data-delay="100">
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
    <img src="images/image-1.jpg" alt="" />
</div>
```
### Trigger on sub-elements IMG, with a delay of 100ms between each call

```html
<div class="has-scrollanim" data-childselector="img" data-usechildren="1" data-delay="100">
    <p>
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
        <img src="images/image-1.jpg" alt="" />
    </p>
</div>
```

### Listen for an event instead of using classnames

```js
document.getElementById('has-scrollanim-element').addEventListener('activescrollanim',function(){
    alert('Scroll has reached this element.');
});
```
