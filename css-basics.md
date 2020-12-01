# CSS Basics

CSS stands for Cascading Style Sheets and is the core component in the presentation layer of all websites you see and use everyday. CSS is a bag of tricks and is often either loved or hated for it. As you'll see, CSS doesn't play like most other programming languages and for that reason developers from traditional programming backgrounds have distanced themselves from it.

But with a bit of time and getting lost in the world of how to center a div to navigating flexbox you will understand its importance and its symbiotic relationship with HTML and JavaScript, and why it is such an important partner within that relationship. 

### Why does it *cascade*? 

CSS is a waterfall. It flows from the top to the bottom but is rendered by your browser from the bottom to the top. This means that understanding hierarchy; which selectors have precedence over others, why you would set a property value at the top of the sheet and not the bottom and how the whole language flows into and past itself - will save you a lot of time in your future CSS debugging days. 

### The relationship with HTML 

HTML by itself is just boring. Browsers have their own specific user style sheet that presents native HTML in a simple, bare-bones style. By adding a CSS stylesheet to this HTML document, we can breathe life into the HTML, make it more accessible, and help it adapt to different screen sizes. 

## Okay, show me some CSS

No worries. A CSS statement is made up of three parts. The selector, the property and the value. Say we want our H1 tags to be red and massive, like 100px. We can do that through CSS:

```css
h1 {
    font-size: 100px;
    color: red;
}
```
Viola! We've done it. Here, our `selector` is the H1 tag. We've said to the stylesheet to find all of the H1 tags in the document, and apply our styles. So `selector` = find this thing. Cool. 

Next, we set our css **properties**. These are properties of the selector we have chosen and give CSS an idea of what they should focus on, once it is scoured your HTML and found what you want it to find. Here, our properties are the `font-size` and `color`. We're telling our CSS to find the H1 and be ready to change its size and color. 

Finally, we have our **values**. These are the levers of CSS and allow us to move things around and build things specific to the project you're working on. Here, we've set the values to be our red color and our massive 100px text size. 


## Adding a stylesheet to a HTML document 

CSS can be integrated into a HTML document in two ways: 

#### Internal CSS

We use an native HTML `<style>` tag to write our CSS. We can put our style tag anywhere within the HTML tags and it will render within the HTML document. 

```html
<!DOCTYPE html>
<html lang="en">
    <style>
        h1 {
            font-size: 100px;
            color: red;
        }
    </style>
<body>

    <h1>Hello world</h1>

</body>
</html>
```

#### External CSS

Here we use the `<link>` tag within our `<head>` tags to link to an external CSS file within the projects parent directory, asset folder or some CDN if you're using a framework like Twitter Bootstrap. 

```html
<!DOCTYPE html>
<html lang="en">
<link rel="stylesheet" href="style.css">
<body>

    <h1>Hello world</h1>

</body>
</html>
```

### Progressive Enhancement

An external stylesheet is the preferred method of most developers due to the concept of **progressive enhancement**. Progressive enhancement is the concept that the content, presentation and behaviour layers of modern web pages should be held separately from one another. 

Put simply, your project should have a separate HTML, CSS and JavaScript file. I won't go too much into why but beyond accessibility, it allows you to work on the individual layers of your project without any conflict between them. [Praveen Dubey has a good take on its importance in web design.](https://www.freecodecamp.org/news/what-is-progressive-enhancement-and-why-it-matters-e80c7aaf834a/)


