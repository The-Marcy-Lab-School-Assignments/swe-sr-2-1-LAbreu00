# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:

- Examples of semantic and non-semantic tags
- The differences between semantic and non-semantic tags
- The benefits of using semantic tags (when possible)

### Response 1

- Examples of **sematic** tags are `<header>` and `<footer>`
- Examples of **non-sematic** tags are `<div>` and `<p>`

The difference between **sematic** and **non-semantic** tags are that **semantic** tags are more descriptive in their names, making your code much more legible. `<header>` is gives more information to the reader at first glance when compared to something like`<p>` so making your code more readable and organized is a big reason to use **sematic** tags.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2

- Some ways to make your code more accessible is to add **descriptions** to an image for those who can't see very well, or making clickable areas **larger** for those that have a hard time with precision.

It's important for developers to consider these accessibility features because we want the tech and projects that we make to be **available** to the largest amount of people possible, from both a consideration stand point but also a feedback standpoint.

- The more people that touch your project, the more feedback you can get on it, and continue to iterate and improve for those who use the technologies you develop.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;">hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

- One reason why using "inline" CSS styles could be useful could be its convenience. Having your styles and content all in one place could make it easier to look at when trying to just glance at your code.
- Having separate CSS and HTML files is more beneficial however because of the design principle **separation of concerns**. Having these two code files separate makes each file have its own "concern", or in other words, makes _managing_ the purpose of each file easier.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

- An explanation of the concept of "classes" and "ids" with an analogy.
- An example of the usage using an HTML code block and a CSS code block.
- An explanation of the syntax using the terms: **attribute**, **selector**

### Response 4

In HTML,`classes` and `ids` labels used to identify or group together elements. Think of `classes` like an actual classroom of students with `ids` being the individual students in the class.

Here's an example:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>School</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <ul class="homeroom">
      <h2>Homeroom 1</h2>
      <li id="nathan">This is Nathan, his favorite color is green</li>
      <li id="mac">This is Mac, his favorite color is red</li>
      <li id="patricia">This is Patricia, her favorite color is orange</li>
    </ul>
    <ul class="homeroom">
      <h2>Homeroom 2</h2>
      <li>Student 1</li>
      <li>Student 2</li>
      <li>Student 3</li>
    </ul>
  </body>
</html>
```

```css
.homeroom {
  font-family: monospace;
  font-weight: bold;
}

#nathan {
  color: green;
}

#mac {
  color: red;
}

#patricia {
  color: orange;
}
```

In our example we have an some HTML with two `ul`(unordered list) tags containing three student `li`(list) elements each. we also have a CSS file with some `selectors` and styles.

- we've added some `attributes` to the unordered lists and the list items tags. `Attributes` add more information into the opening tag of a given element, in our example, these are our `class` and `ids`.

- `Selectors` are how we designate what CSS styles to apply to what HTML code. In our example, **homeroom** is our `class`, using the `.homeroom` notation, while the students **individual names** are the `ids`, using a `#` instead (ex. `#mac`).

- `Classes` are identifiers meant to be used more **broadly**. In our example we see our **homeroom** `class` appear twice, once for homeroom 1 and again for homeroom 2. That means that the same CSS style will be applied to both of the unordered lists.

- `Ids` are meant to be unique identifiers, so they'll only ever be seen in one tag. in our example, the CSS style that are applied to the individual `ids` are the student's favorite colors. Those `ids` won't show up more then once in our HTML, and those styles will only ever apply to the the element/s with that unique `id` attribute in its tag.

## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

When building a website, its important to consider the content that's **static** and the content that's **dynamic**.

- If there's content that won't be interacted with by the user, then it can be incorporated into the `HTML` file as a **static** element. Think things like a heading, or the names of sections on a website.
- If the content needs interactivity or will be changed in any way by user input, then that's **dynamic** content that's better suited for `JavaScript`. Things like buttons or forms that require moving parts are fall under this category.
