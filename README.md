# Exam: HTML & CSS

### Getting Started
 - Fork this repository under your own account
 - Commit your progress frequently and with descriptive commit messages
 - All your answers and solutions should go in this repository

### What can I use?
 - You can use any resource online, but **please work individually**
 - Instead of copy-pasting your answers and solutions, write them in your own words.


# Tasks

## 1. Build a design (~90 minutes) [10 points]
Build the following profile cards according to the design provided.   
Follow the design as closely as possible.   
Commit an HTML and a CSS file to this repository.
![design](exercise-1.png)

### Assets
John Duck | Jane Duck | Pencil icon
--------- | --------- | -----------
![duck](duck.jpg) | ![duck](duck2.jpg) | ![pencil-icon](edit-icon.png)   

### Other data
  - Name font size: 28 pixels
  - Text size: 14 pixels
  - Font family: Arial, sans-serif

### Acceptance criteria
The task is accepted if:
  - The result follows design [2p]
  - The code follows style guide [1p]
  - The CSS & HTML are valid [1p]
  - The HTML considers semantic responsibilities [2p]
  - The code avoids code duplication [2p]
  - The CSS has meaningful and short selectors [2p]

Extra points for if:
  - the result is centered on the page [2p]


## 2. Understand code (~15 minutes) [2 points]
Read the following code snippet:   
What is the distance between the top-left corner of the document body and the yellow box?   
Give a detailed explanation below!   
Add your answer to this readme file, commit your changes to this repository.
```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        padding: 0px;
        margin: 0px;
      }
      .foo {
        top: 20px;
        left: 20px;
        width: 100px;
        height: 100px;
        position: absolute;
        background: blue;
      }
      .bar {
        top: 20px;
        left: 20px;
        width: 30px;
        height: 30px;
        position: absolute;
        background: yellow;
      }
    </style>
  </head>
  <body>
    <div class="foo">
      <div class="bar"></div>
    </div>
  </body>
</html>
```
#### Your answer: [2p]
The distance between the top-left corner of the body and the yellow box is 56.57px. This is according to the Pythagorean theorem, but I guess my answer should be 40px down and 40px from the left. This is because:

1. There's no padding or margin on the body or any of the divs.

2. Both divs' positions are set to absolute, so their positions are compared to their parent divs.

3. The `.bar` div is within the `.foo` div, therefore their positions add up.


## 3. Explain concepts (~15 minutes) [4 points]
Add your answer to this readme file, commit your changes to this repository.


### Explain the difference between `display: block` and `display: inline` in CSS! What is `display: inline-block`?
#### Your answer: [2p]
`display: block` blocks out the entire width of the parent element for the element it is set to. It follows the box-model. Example: `<div>` On the other hand, `display: inline` is only as wide as the width of the actual element, therefore several elements can be in one line. Example: `<span>` `display: inline-block` lets us use the best of both: it allows width and height for elements but also allows them to flow next to each other on one line.


### What is the difference between a `<section>` and an `<article>` element? Name one good example of using an `<article>`.
#### Your answer: [2p]
These are both used to define semantical differences, rather than syntactical. A `<section>` element usually has a separate heading and text that belongs to it. It's content belongs together. Whereas `<article>` refers to a bigger block of text that is one unit. `<section>` can be within an `<article>` `<article>` can be used for content that is allowed to be distributed separately from the rest of the website. (I swear I didn't steal this from w3 schools, but I saw afterwards that they explained it with the exact same wording.) Example: Blog post.