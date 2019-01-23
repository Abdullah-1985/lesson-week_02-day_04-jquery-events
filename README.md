# jQuery

## jQuery Selectors

<img width="800" alt="screen shot 2019-01-22 at 10 23 23 am" src="https://user-images.githubusercontent.com/5384023/51586809-b2f61700-1eef-11e9-89d2-973da0751213.png">

## jQuery Manipulate DOM

<img width="800" alt="screen shot 2019-01-22 at 10 24 49 am" src="https://user-images.githubusercontent.com/5384023/51586815-b4274400-1eef-11e9-9e04-f587b0d2eb23.png">

<img width="806" alt="screen shot 2019-01-22 at 10 25 24 am" src="https://user-images.githubusercontent.com/5384023/51586819-b6899e00-1eef-11e9-8897-9f845871a209.png">

## jQuery Animations

<img width="800" alt="screen shot 2019-01-22 at 10 25 37 am" src="https://user-images.githubusercontent.com/5384023/51586821-b8536180-1eef-11e9-9ff3-1a0b98e57f46.png">

Discuss and experiment with
- [.hide()](https://api.jquery.com/hide/)
- [.show()](https://api.jquery.com/show/)
- [.toggle()](https://api.jquery.com/toggle/)
- [.fadeIn()](https://api.jquery.com/fadeIn/)
- [.fadeOut()](https://api.jquery.com/fadeOut/)
- [.slideUp()](https://api.jquery.com/slideUp/)
- [.slideDown()](https://api.jquery.com/slideDown/)
- [.animate()](https://api.jquery.com/animate/)

### Lab: jQuery Animations
Open [exercise/jquery-animations/index.html](exercise/jquery-animations/index.html) in your browser.

Open [exercise/jquery-animations/](exercise/jquery-animations/) folder in your text editor.

Complete the exercises in [exercise/jquery-animations/main.js](exercise/jquery-animations/main.js). You will see the results in the browser console.

Read more about [jQuery effects and animations](https://api.jquery.com/category/effects/)

View the [jQuery cheatsheet](https://oscarotero.com/jquery/)

## jQuery Events

DOM Events are sent to notify code of interesting things that have taken place. Each event is represented by an object which is based on the Event interface, and may have additional custom fields and/or functions used to get additional information about what happened. Events can represent everything from basic user interactions to automated notifications of things happening in the rendering model.

<img width="800" alt="screen shot 2019-01-23 at 9 40 11 am" src="https://user-images.githubusercontent.com/5384023/51587830-264d5800-1ef3-11e9-8b4d-0474fd76447a.png">

If you'd like to see more events, check out the [full list of DOM events](https://developer.mozilla.org/en-US/docs/Web/Events).  Many are consistent throughout various browsers but some are specific to a browser.

jQuery has methods we can use for specific events like `.click()`.  However, the preferred way to do events with jQuery is by using the [`.on()`](http://api.jquery.com/on/) method.

```js
function printHello () {
    console.log('Hello');
}

$('h1').on('click', printHello);
```

We can combine events and other jQuery methods to build our interactive web pages.

```js
function changeBackground () {
    $('body').css('background-color', 'red');
}

$('h1').on('click', changeBackground);
```

We can listen for hover events:
```js
function increaseFont () {
    $('h1').css('font-size', '100px');
}

$('h1').on('hover', increaseFont);
```

We can listen for forms submitting:

```html
<form>
   <input type='text'>
   <input type='submit' value='Submit Form'>
</form>
```
```js
function printUserInput (event) {
    event.preventDefault()
    let userInput = $('input:first-child').val();
    console.log(userInput)
}
$('form').on('submit', printUserInput)
```

What is the `event` key word?

### Lab: jQuery Events

Open [exercise/jquery-events/index.html](exercise/jquery-events/index.html) in your browser.

Open [exercise/jquery-events/](exercise/jquery-events/) folder in your text editor.

Complete the exercises in [exercise/jquery-events/main.js](exercise/jquery-events/main.js). You will see the results in the browser console.

### Lab: Color Scheme Picker

Open [exercise/color-scheme-picker/index.html](exercise/color-scheme-picker/index.html) in your browser.

Open [exercise/color-scheme-picker/](exercise/color-scheme-picker/) folder in your text editor.

Complete the exercises in [exercise/color-scheme-picker/js/main.js](exercise/color-scheme-picker/main.js). You will see the results in the browser console.

### Lab: Traffic Light

Open [exercise/traffic-light/index.html](exercise/traffic-light/index.html) in your browser.

Open [exercise/traffic-light/](exercise/traffic-light/) folder in your text editor.

Complete the exercises in [exercise/traffic-light/js/main.js](exercise/traffic-light/main.js). You will see the results in the browser console.