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

### Rules, glorious rules. 

CSS is made up of rules, much like HTML is made up of elements and JavaScript of statements. These rules can apply to one specific selector or multiple. 

Let's say for example, that we want to set all `p` and `h6` tags to the colour blue. But the `h2` and `h1` tags, to orange. By adding a `,` separator between the selectors when declaring the rule, we can target multiple selectors in one rule. 

```css 
p, h6 {
    color: blue; 
}

h1, h2 {
    color: orange; 
}
```

We can extend this rules further when we start to the think in terms of `classes` by being more specific with our rules to apply styles to elements *within* a class, not just limited to global styles on all element tags. 

### The waterfall rule 

That's not CSS jargon, just something I like to remember when applying CSS rules. The main rule is: **Anything on the bottom of the stylesheet, takes precedence over other previously declared styles.**

Going back to our previous example of where we set all of the `p` tags to blue. If we do something like this, the `p` tags will now be blue. This is the waterfall rule. The browser will only render the last cascaded style. However, you see how `text-align` is now `center`, this will be **inherited** by the new red `p` tag.

When style is only superseded by a re-declaration of a selector rule when the property value is changed and only that specific value will take effect. 

```css 
p, h6 {
    color: blue;
    text-align: center; 
}

p {
    color: red;
}
```

### Classes & ID's

Classes and ID's are a core component in the flexibility of CSS. Up until now, we have been setting our styles globally to the HTML element tags. But with classes and ID's, we can apply styles to specific elements and reuse the styles where we want.

### Classes

To declare a class, we use the `.class` notation. You can name a class whatever you like but just like JavaScript variables, make it meaningful. Let's make a class called `.bkgBlue`. 

```css 
.bkgBlue {
    background: blue;
}
```
This style will now set the background blue on whatever element we apply the class to. To actually use this class, we have apply it to a HTML element. Let's set the first `<div>` to blue. 

```html
<!DOCTYPE html>
<html lang="en">
<link rel="stylesheet" href="style.css">
<body>
    <div class="bkgBlue">
        <h1>Hello world</h1>
        <p>I live on GitHub</p>
    </div>
</body>
</html>
```

Pretty easy right? As long as you leave out the `.`, you can now add classes to any element you like and have more control over your styling. 

### IDs

Classes are utilities, in that they can be applied everywhere and anywhere in the HTML document. But what if you have a specific element that you want to style? There, we use an ID. 

Keeping with our previous example, lets set the `h1` to a larger text than its sibling `p` tag. 

```css 
#bigText {
    font-size: 100px;
}
```

```html
<!DOCTYPE html>
<html lang="en">
<link rel="stylesheet" href="style.css">
<body>
    <div class="bkgBlue">
        <h1 id="bigText">Hello world</h1>
        <p>I live on GitHub</p>
    </div>
</body>
</html>
```

