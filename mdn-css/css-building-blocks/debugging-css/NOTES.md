# Debugging CSS #
Sometimes when writing CSS you will encounter an issue where your CSS doesn't seem to be doing what you expect. Perhaps you believe that a certain selector should match an element, but nothing happens, or a box is a different size than you expected. This article will give you guidance on how to go about debugging a CSS problem, and show you how the DevTools can help you find out what's going on.

## The DOM versus view source ##
Something that can trip up newcomers to DevTools is the difference between what you see when you view the source of a webpage, or look at the HTML file you put on the server, and what you can see in the HTML pane of the DevTools. While it looks roughly similar to what you can see via View Source there are som differences.

In the rendered DOM the browser may have corrected some badly-written HTML for you. If you incorrectly closed an element, for instance opening an <h2> but closing with an </h3>, the browser will figure out what you were meaning to do and HTML in the DOM will correctly close the oepn <h2> with an </h2>. The browser will also normalize all of the HTML, and the DOM will also show any changes made by JavaScript.

View Source in comparison, is simply the HTML source code as stored on the server. The HTML tree in your DevTools shows exactly what the browser is rendering at any given time, so it gives you an insight into what is really going on.

## Inspecting the applied CSS ##
A useful ability when inspecting elements with DevTools is the ability to exapnd out shorthand properties. If you click on the little arrow to exapnd the view, it'll show you the different longhand properties and their values.

You can also toggle values in the Rules view on and off, when that panel is active - if you hold your mouse over it checkboxes will appear. Uncheck a rule's checkbox and the CSS will stop applying.

You can also use this to do an A/B comparison, deciding if something looks better with a rule applied or not, and also to help debug it - for example if a layout is going wrong and you are trying to work out which property is causing the problem.

## Editing Values ##