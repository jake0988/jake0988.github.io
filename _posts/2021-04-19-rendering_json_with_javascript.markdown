---
layout: post
title:      "Rendering JSON With Javascript"
date:       2021-04-20 00:53:38 +0000
permalink:  rendering_json_with_javascript
---


In order to create a single page web app with JavaScript, our html index page only needs one element. From this element we can attach an unlimited amount code. In some cases it may be much simpler if our index has more html elements to create a skeleton for our JavaScript to attach to, but this example will only deal with a single list.
This example uses only a single <div>.

[https://imgur.com/3wZMxW2]
Notice that the div has an id of “example.”

From that div we need to attach all of the code in this example.
First, add an event listener, so that when the page loads a <button> element is created.

https://imgur.com/tH1cbk0
On page load, we find the div, create a <button> element, format the <button>, and attach it to the div.

https://imgur.com/mcWB5hE
The webage now has a <button> element.

Now we want the <button> to be clickable, so we create another event listener that responds to mouse clicks. However, because our listener is attached to the document node, anywhere on the webpage will respond equally to the click. We can make it so that the code only responds to <button> clicks by using a an if statement to see if the click event came from the <button>.
https://imgur.com/fCtnPyA


https://imgur.com/2xdVfun
In order to find out what to look for when checking for equality in the if state, use Chrome's debugger to see a list of possible queries to use.


To get information to render on the page, I have created an Adapter class that makes fetch calls to a rails server. The function fetchCustomers() retrieves a JSON response. We create an unorder list element to put list items in. For each JSON object, an <li> is created, and each attribute in the response that we want rendered into that list item. Then the list item is the appended to the <ul>. Finally, the <ul> is attached to the <<button>>.
https://imgur.com/bPKkgni

https://imgur.com/oIGZoR8
The final look of the webage

Although this example only rendered three first names and put them in a list, it is easy to imagine any amount of information being added in this manner. Using javascript not only alows for content to be added dynamically, it also allows you to change the look of the webpage by interacting with it. Any amount of information can be displayed in this manner, and it can be manipulated in any way the dom is capable of manipulating data.
