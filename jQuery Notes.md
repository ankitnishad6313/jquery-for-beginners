### jQuery Syntax

#### Basic Syntax of jQuery:

```javascript
$(document).ready(function () {});

jQuery(document).ready(function () {});

// Only in body tag
$(function () {});

// In Javascript
document.getElementByTagName("h1");

// In jQuery
$("h1");

// Id Selector
document.getElementById("para");

$("#para");
```

### Mouse Events

1. **`click()`**: Triggered when an element is clicked.
2. **`dblclick()`**: Triggered when an element is double-clicked.
3. **`mouseover()` / **`mouseenter()`\*\*: Triggered when the mouse pointer enters the element.
4. **`mouseout()` / **`mouseleave()`\*\*: Triggered when the mouse pointer leaves the element.
5. **`contextmenu()`**: Triggered when the right mouse button is clicked (context menu).

### Keyboard Events

1. **`keypress()`**: Triggered when a key is pressed (deprecated in recent versions).
2. **`keydown()`**: Triggered when a key is pressed down.
3. **`keyup()`**: Triggered when a key is released.

### Get and Set Methods

1. **`html()`**: Gets or sets the HTML content of an element.
2. **`text()`**: Gets or sets the text content of an element.
3. **`val()`**: Gets or sets the value of form elements like input and select.
4. **`data()`**: Gets or sets data attributes associated with the element.
5. **`attr()`**: Gets or sets attributes of the element.

### Form Events

1. **`focus()`**: Triggered when an element gains focus.
2. **`blur()`**: Triggered when an element loses focus.
3. **`select()`**: Triggered when text is selected in a text field.
4. **`change()`**: Triggered when the value of an element changes.
5. **`submit()`**: Triggered when a form is submitted.
6. **`reset()`**: Triggered when a form is reset.

### Window Events

1. **`load()`**: Triggered when the entire page (including images) has loaded (removed in jQuery > 3).
2. **`unload()`**: Triggered when the page is unloaded (removed in jQuery > 3).
3. **`resize()`**: Triggered when the window is resized.
4. **`scroll()`**: Triggered when the window or an element is scrolled.

# https://github.com/ankitnishad6313/

# jQuery Methods Documentation

### 1. **hide(), show(), and toggle()**

These methods control the visibility of elements.

- **`hide()`**: Hides the selected element.
- **`show()`**: Shows the hidden element.
- **`toggle()`**: Toggles between hiding and showing the element.

### 2. **empty() and remove()**

Used to manipulate the content of elements.

- **`empty()`**: Removes all child elements from the selected element.
- **`remove()`**: Removes the selected element itself, including its child elements.

### 3. **append() and prepend()**

Used to insert content inside an element.

- **`append()`**: Inserts content at the end of the selected element.
- **`prepend()`**: Inserts content at the beginning of the selected element.

### 4. **after() and before()**

Used to insert content outside the element.

- **`after()`**: Adds content immediately after the selected element.
- **`before()`**: Adds content immediately before the selected element.

### 5. **addClass(), removeClass(), and toggleClass()**

Used for managing CSS classes of elements.

- **`addClass()`**: Adds a class to the selected element.
- **`removeClass()`**: Removes a class from the selected element.
- **`toggleClass()`**: Toggles a class on or off.

### 6. **on() and off()**

- **`on()`**: Attaches an event handler to the selected elements.
- **`off()`**: Removes an event handler from the selected elements.

### 7. **clone()**

Creates a copy of the selected element, including child elements and attributes.

### 8. **appendTo() and prependTo()**

- **`appendTo()`**: Inserts the selected elements into another target element at the end.
- **`prependTo()`**: Inserts the selected elements into another target element at the beginning.

### 9. **wrap() and unwrap()**

- **`wrap()`**: Wraps the selected elements inside a specified structure (e.g., `<div>`).
- **`unwrap()`**: Removes the parent structure from the selected elements.

### 10. **replaceWith() and replaceAll()**

- **`replaceWith()`**: Replaces the targeted elements with either HTML elements or strings.
- **`replaceAll()`**: Replaces the targeted elements with only HTML elements.

### 11. **height() and width()**

- **`height()`** and **`width()`**: Return the element's height and width.
- **`innerHeight()`** and **`innerWidth()`**: Include padding.
- **`innerHeight(true)`** and **`innerWidth(true)`**: Include padding, border, and margin.

### 12. **position() and offset()**

- **`position()`**: Returns the element's position relative to its parent.
- **`offset()`**: Returns the element's position relative to the document.

### 13. **fadeIn(), fadeOut(), fadeToggle(), and fadeTo()**

Used for fading effects:

- **`fadeIn()`**: Fades the element into view.
- **`fadeOut()`**: Fades the element out of view.
- **`fadeToggle()`**: Toggles between fading in and out.
- **`fadeTo()`**: Fades the element to a specific opacity.

### 14. **hasClass()**

Checks if the selected element has a specific class and returns a boolean.

### 15. **wrapAll() and wrapInner()**

- **`wrapAll()`**: Wraps all selected elements inside a single structure.
- **`wrapInner()`**: Wraps the content of each selected element inside a structure.

### 16. **scrollTop() and scrollLeft()**

- **`scrollTop()`**: Gets or sets the vertical scroll position of an element.
- **`scrollLeft()`**: Gets or sets the horizontal scroll position of an element.

### 17. **Ajax Syntax**

```javascript
$.ajax({
  url: "", // URL of the resource
  method: "", // HTTP method: GET, POST, PUT, PATCH, DELETE
  data: {}, // Data to be sent
  dataType: "JSON", // Expected data type

  success: function (response) {
    // Handle successful response
  },

  error: function (xhr, error, status) {
    // Handle errors
  },

  beforeSend: function () {
    // Any operations to perform before sending
  },

  complete: function () {
    // Runs regardless of success or error
  },
});
```

# jQuery Ancestor Methods

## 1. `parents()`
Selects all ancestor elements of the selected element, all the way up to the document's root element.

**Example:**
```javascript
$(".child").parents("div");
```

## 2. `parent()`
Selects the immediate parent of the selected element.

**Example:**
```javascript
$(".child").parent();
```

## 3. `parentsUntil()`
Selects all ancestor elements between the specified element and a stopping point.

**Example:**
```javascript
$(".child").parentsUntil(".container");
```

## 4. `offsetParent()`
Returns the first ancestor element that is positioned (relative, absolute, or fixed).

**Example:**
```javascript
$(".child").offsetParent();
```

## 5. `closest()`
Selects the closest ancestor of the selected element (can include itself) that matches the selector.

**Example:**
```javascript
$(".child").closest("div");
```

# jQuery Descendant Methods

## 1. `children()`
Selects all immediate children of the selected element.

**Example:**
```javascript
$(".parent").children(".child");
```

## 2. `find()`
Selects all descendant elements of the selected element that match the selector.

**Example:**
```javascript
$(".parent").find(".child");
```

# jQuery Siblings Methods

## 1. `next()`
Selects the immediate next sibling of the selected element.

**Example:**
```javascript
$(".item").next();
```

## 2. `nextAll()`
Selects all next siblings of the selected element.

**Example:**
```javascript
$(".item").nextAll();
```

## 3. `nextUntil()`
Selects all next siblings up to (but not including) the element matched by the selector.

**Example:**
```javascript
$(".item").nextUntil(".stop");
```

## 4. `prev()`
Selects the immediate previous sibling of the selected element.

**Example:**
```javascript
$(".item").prev();
```

## 5. `prevAll()`
Selects all previous siblings of the selected element.

**Example:**
```javascript
$(".item").prevAll();
```

## 6. `prevUntil()`
Selects all previous siblings up to (but not including) the element matched by the selector.

**Example:**
```javascript
$(".item").prevUntil(".start");

# jQuery Animation Methods

## 1. `animate()`
Performs a custom animation on the selected elements by changing CSS properties.

**Parameters:**
- **`properties`**: An object of CSS properties and values to animate.
- **`duration`**: Specifies the speed of the animation (e.g., "slow", "fast", or milliseconds).
- **`easing`**: Specifies the easing function (optional).
- **`complete`**: A function to call once the animation is complete (optional).

**Example:**
```javascript
$(".box").animate({
  width: "200px",
  height: "100px"
}, "slow", function() {
  console.log("Animation complete!");
});
```
## 2. `stop()`
Stops the currently running animation on the selected elements.

**Parameters:**
- **`clearQueue`**: A boolean value that indicates whether to remove animations queued for the element (optional, default is `false`).
- **`jumpToEnd`**: A boolean value that indicates whether to complete the current animation immediately (optional, default is `false`).

**Example:**
```javascript
$(".box").stop(true, true);
```
