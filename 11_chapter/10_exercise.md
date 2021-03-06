**WDI Fundamentals Unit 11**

---

##![Your Turn](../assets/exercise.png) Your Turn

Now that we have a way to store keys and values, we can add some complexity to our contact book. Are you ready?

Again, our goal is to create a contact book that allows us to store contact info (including first name, last name, phone, and email address), add a new contact, list contacts, and find contacts by first or last name.

Before reading the instructions below, take a few minutes to think through the problem and try your hand at writing out pseudocode. Although the instructions will guide you through the steps for building the program, it's helpful to practice thinking about your own approach. Programmatic thinking becomes easier with practice!

## Instructions

1) Write the code to perform the actions listed below using JS Bin editor. If you don't see the JS Bin, please refresh the page.
2) Click "Run" to run the code in the "Console" panel.
3) Call each function from the "Console" panel. Try using different parameters to make sure they're working properly.

<a class="jsbin-embed" href="http://jsbin.com/hotibob/embed?js&height600">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.39.19"></script>

### Let's get started!

* Create an array called `contacts`. The `contacts` array should contain three objects, one for each contact stored in our book. Here's the contact information for each person:

| 'firstName' |  'lastName' |  'phone'        |    'email'           |
|-            |-            |-                |-                     |
| 'John'      |   'Doe'     |'(512) 355-0453' |'johndoe@email.com'   |
| 'Jane'      |   'Doe'     |'(312) 641-2203' |'janedoe@email.com'   |
| 'Suzie'     |   'Smith'   |'(415) 604-4219' |'suziesmith@email.com'|

* Next, let's create a function, `addContact`, that accepts one parameter, `newContact`. This function should add the parameter to the end of the `contacts` array and return the `contacts` array. When you're done, try calling the function and passing in an object as a parameter to make sure it's working.
* Now, let's create a `listContacts` function to list our contacts. This function should loop through the `contacts` array and log the first and last name for each contact to the console, i.e. `'John Doe'`.
* Finally, let's create a function that will search through our `contacts` array and return the contact info for any person who has a matching first or last name. Create a `search` function, which will take one parameter, `name`. In the `search` function, use a loop to iterate through the `contacts` array and return the current contact if his or her first *or* last name matches the `name` parameter.

You've done it! We now have a working contact book that allows us to store contacts, add contacts, list contacts, and find a contact by first or last name. Congratulations!

> *Stuck? Check out the [solutions](../exercise-solutions.md) to see what you can do.*

---

Feeling confident? [Test your understanding of iteration with this next quiz.](09_quiz.md)
