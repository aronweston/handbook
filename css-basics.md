# CSS Basics

CSS stands for Cascading Style Sheets and is the core component in the presentation layer of all websites you see and use everyday. CSS is a bag of tricks and is often either loved or hated for it. As you'll see, CSS doesn't play like most other programming languages and for that reason developers from traditional programming backgrounds have distanced themselves from it.

But with a bit of time and getting lost in the world of how to center a div to navigating flexbox you will understand its importance and its symbiotic relationship with HTML and JavaScript, and why it is such an important partner within that relationship. 

### Why does it *cascade*? 

CSS is a waterfall. It flows from the top to the bottom but is rendered by your browser from the bottom to the top. This means that understanding hierarchy; which selectors have precedence over others, why you would set a property value at the top of the sheet and not the bottom and how the whole language flows into and past itself - will save you a lot of time in your future CSS debugging days. 

### The relationship with HTML 

HTML by itself is just boring. Browsers have their own specific user style sheet that presents native HTML in a simple, barebones style. By adding a CSS stylesheet to this HTML document, we can breathe life into the HTML, make it more accessible, and help it adapt to different screen sizes. 


## Adding a stylesheet to HTML document 

CSS can be integrated into a HTML document in two ways: 

1. Internal CSS: we use an native HTML ```html <style></style> tag to 






Let's give it a go (feel free to chuck this into your browser)

```html
<!DOCTYPE html>
<html lang="en">
<body>

    <h1>Hello world</h1>

</body>
</html>
```

Pretty boring, right

