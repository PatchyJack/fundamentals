**WDI Fundamentals Unit 10**

---

##![Your Turn](../assets/exercise.png) Your Turn

Here's the starter code for your next exercise. If you don't see the JS Bin below, please refresh the page.

<a class="jsbin-embed" href="http://jsbin.com/gokecos/1/embed?html&height600">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.35.12"></script>

Let's get some practice manipulating the DOM and adding some interactions to our reading list.

###Instructions

1) Let's get started! Some starter code has been provided in the JS Bin for this exercise.
2) Write the code to perform the actions listed below in the "JavaScript" panel.
3) Click "Run" to see the results in the "Console" panel.

**Let's get started!**

* We've finished reading *The Wind Up Bird Chronicle* and *A Visit From the Goon Squad*! Use the `getElementsByClassName()` to find all elements with the `current` class. Then, use a `for` loop to iterate through these elements and change the class name to `finished`.

* Now, on to our next book on the reading list, *The Flamethrowers*. Use the `getElementById()` method to find that list item. Update its class name to `current`. Then, use the `removeAttribute()` method to remove the `id` attribute.

* Now, find the fourth list item and update the `id` attribute to `next` using the `setAttribute()` method.

* When a user clicks on the button with the ID `chill`, loop through all list items and add the class `cool` to each. Test it out! Each list item should have a blue border after the user clicks on its button.

* When the user clicks on the first list item, add an item to the end of the list that says "JavaScript is Fun!"


Feeling confident? [Test your understanding of functions and the DOM with this next quiz.](12_quiz.md)
