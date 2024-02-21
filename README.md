# Practical 3 (Week 2) - CSS Fundamentals

This practical is all about getting you started with CSS to add style to your HTML documents. 

## Stage 1: CSS Selector Familiarisation
Play [CSS Diner](https://flukeout.github.io/). This game will introduce you to some selectors we didn’t cover in class. Try to complete as many levels as you can, but you can stop after level 16 if you get frustrated! 

_Aim to spend no more than 30 minutes on this task!_

## Stage 2: Writing Internal Styles
The three exercises in this stage walk you through a few useful text styling approaches and a few less commonly used CSS properties. You will need the HTML files available in this repository.
Open the three files (exercise2_1.html, exercise2_2.html, exercise 2_3.html) in VS Code. You will notice that each file is identical. Your task is to add internal CSS to each file to produce the expected output.

For each exercise, you will need to add `<style></style>` elements inside the `<head>` of the HTML file, then add your CSS inside the `<style>` elements. **You must only write code inside the `<style>` elements—do not modify the rest of the HTML in any way. **

Links to relevant documentation are provided in places. Keep the CSS documentation (either MDN or W3Schools, or both) handy as you work. You can also try typing properties straight into VS Code and exploring the auto-complete suggestions.
### Exercise 2.1: Styling with pseudo selectors
Style exercise2_1.html so it looks a bit like an old book, as pictured below. Links to the relevant properties and additional guidance is provided after the screenshot. 

![Screenshot of the final result for Ex2.1](https://github.com/IM-WADD/Week2Practical1/assets/5978932/a19d39b8-2265-41a0-aed9-f2f6dbace3ee)

The key features are:
- Additional spacing around the edge of the “page” to increase readability.
- An off-white background colour for the body and a dark grey text colour.
- A serif font-family for the heading and first paragraph only.
- The first paragraph has a larger font-size than the others.
- A sans-serif font-family for the remaining paragraphs.
- The line-height of all paragraphs is bigger than default to increase readability.
- All paragraphs are justified (an alignment option).
- The first letter of the first paragraph has additional decorative styling.

If you have substantial CSS experience, try to create the expected output without following the guidance below!

_**Step-by-step guidance**_
1. Add a `body` selector to your CSS section. Then, in the declaration following the `body` selector, set the following properties: `background-color`, `color`, and `padding` with values of your choosing. There should now be more space between the text and the left and right edges of the screen, and the background and text colours should look a bit more book-like.
2. Next, set the font families. You will need a selector and declaration for the `h1` element, a separate selector and declaration for the `p` elements, and an additional selector and declaration that will use the [:first-of-type pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/:first-of-type) to give the first paragraph a different font than the others. You can choose the specific font families, but the heading and first paragraph should have a serif `font-family`, while the other paragraphs be sans-serif.
3. Add rules to the declaration for `p` elements that set values for `line-height` and `text-align`. The line height should be a little larger than default (experiment!) to increase the space between lines in a paragraph. The alignment should be justified. The `font-size` of the first paragraph also needs to be made bigger than other paragraphs.
4. Finally, you are ready to style the first letter of the first paragraph. You will need to add a new selector to your CSS. You should already know how to write a selector for the first paragraph if you’ve completed step 2. To select the first letter of the first paragraph, add the [::first-letter](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter) pseudo-selector immediately  after the first paragraph selector. To create the decoration shown in the screen shot, I set rules for the following properties: 
- `font-size` (bigger than the rest of the paragraph)
- `font-weight` (bolder)
- `margin-right` (added extra space following the letter)
- `padding` (to create more space between the letter and its border)
- [border](https://css-tricks.com/almanac/properties/b/border/) (using “double” style and a thicker weight than default)

### Exercise 2.2: Creating hover effects
A key principle of interaction design that you should already be familiar with is _feedback_ for user interaction. If an element is interactive, the UI should provide hints that the user can interact with it. In web design, clickable elements often have hover effects—style changes that appear when the user’s mouse is over the element. This is achieved using the [:hover](https://www.w3schools.com/cssref/sel_hover.php) selector, which is commonly used for links but can be applied to other elements as well.
Style exercise2_2.html as follows.

![Image example for Ex2.2](https://github.com/IM-WADD/Week2Practical1/assets/5978932/6149cb4e-10d6-4829-b479-795053f85dbe)

Add spacing around the content for readability and choose a font for all text. 

Give the heading element a background colour and set the text colour to something that clearly contrasts with the background colour. Use the `border-bottom` property to create a solid line in a different colour to the background. Use `padding` to add spacing around the content of the heading so that the text is not bunched up against the edge of the heading background colour. You may find that the text, "Chapter 1", now looks indented compared to the following paragraphs. A handy trick to correct this effect and keep all text aligned is to use negative values for `margin-left` and `margin-right` on your heading element. The value should be the same as the `padding` value, but negative e.g. if you set `padding` to 12px, set `margin-left` and `margin-right` to -12px. 

Next, add a hover effect to the heading element using a new selector, `h1:hover`, to declare style rules to be applied only when the mouse is over the heading. When the heading is hovered, change its text and border colour.

![Image example for hover on title](https://github.com/IM-WADD/Week2Practical1/assets/5978932/fdb31348-6987-4adf-8306-9861a798d16b)

Finally, add hover effects to the paragraph elements. When the mouse is over a paragraph, change its colour and use the [text-transform](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform) property to convert it to uppercase text. Make the paragraph appear to shift 5 pixels right and down. You can achieve this in a few different ways...

![Image example for on hover of paragraph](https://github.com/IM-WADD/Week2Practical1/assets/5978932/888e4ba9-cf0e-4bad-a68a-06e2fd1cf262)

View your completed file in the Chrome device simulator using a simulated touch screen device like an iPhone. What do you notice about the hover effects? Why might this be?

### Exercise 2.3: A few more text styling properties
Give exercise2_3.html some basic styling along the same lines as before: add some spacing around the content for readability and choose a font family for the text. 

Next, [change the orientation](https://developer.mozilla.org/en-US/docs/Web/CSS/text-orientation) of the heading to match the screenshot:

![Example image for Ex 2.3](https://github.com/IM-WADD/Week2Practical1/assets/5978932/8b114b7d-1b71-4d87-90c9-b6cfa0feb7d7)

Notice that a few sentences have been highlighted (black background, white text). The sentences have been selected by the user. By default, browsers allow users to select text elements so that text can be copied or highlighted. The browser will also provide default styling to highlight a text selection (generally a light blue background). Customise the text selection style using the [::selection](https://developer.mozilla.org/en-US/docs/Web/CSS/::selection) pseudo-selector.

You may have noticed that your mouse cursor changes when it is over different types of content on the web. For example, it will often change to a text selection cursor when over text, and a pointer (the little hand) when over something clickable like a link or a button. Some of these changes are provided by default by your browser to communicate the functionality of different elements. You can also control these changes using CSS. Add the appropriate selectors to create new style rules to be applied when a paragraph or heading is hovered. Then, use the [cursor](https://developer.mozilla.org/en-US/docs/Web/CSS/cursor) property to explore different cursors. In particular, try the following values:
- pointer
- wait
- help
- not-allowed
- text

**Interaction design note:** It is usually best to stick with the default cursor provided by the browser as it is already designed to communicate functionality and making changes may cause confusion for the user. However, in the coming weeks, we’ll see use cases for changing the cursor to improve communication of functionality.

## Stage 3: Using External CSS
In this stage, you will create an external stylesheet for the portfolio you started last practical and begin to add basic styling for your site. In the previous stage, you wrote internal CSS. This was appropriate for the stage 2 exercises because there were relatively few styles in each page and the styles only applied to the individual HTML page. When styling a whole website, external stylesheets are recommended as you can reuse styles across pages. External styles also help to separate content and structure from visual styling.

In VS Code, open the folder containing your portfolio site. Create a new file called styles.css. Link the new CSS file to each of your pages by adding the following line to the `<head>` section of each HTML file:
```<link href=”styles.css” type=”text/css” rel=”stylesheet”>```

(Type the line yourself rather than copy-pasting so you don’t end up with character encoding bugs)

Set style rules for your text elements (e.g. font family, weight etc.) and choose a colour palette. Consider setting some margin and padding rules for various elements.

_**Going further**_

If you’d like to explore more advanced styling features than we will cover in lectures, here are a few ideas:
- [Look into using a (free) font delivery service](https://fonts.google.com/knowledge/using_type/using_web_fonts_from_a_font_delivery_service) to enable you to choose from a wider range of fonts.
- Try using a [CSS gradient](https://www.w3schools.com/css/css3_gradients.asp) in place of a solid background colour.
- Add visual depth using [CSS box-shadow.](https://www.w3schools.com/css/css3_shadows_box.asp)https://www.w3schools.com/css/css3_shadows_box.asp

