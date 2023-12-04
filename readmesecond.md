### CUSTOM VARIABLES/PROPERTIES DESCRIPTION ###

So, what are custom variables/custom properties in the first place?
They are essentially variables, just as we know them from JavaScript, but just in CSS.
They let you write a lot more effecient styling, and they make it 100 times faster to change the whole theme of a web page
by just changing one value in one place.

### DECLARING AND ASSIGNING CUSTOM VARIABLES/PROPERTIES ###
So, how do we write, and where do we define a custom variable/custom property?

The custom variables are defined in what's called the root scope.
To get to the root scope, we write ":root" and follow it by "{}".

So, once we have access to the root scope, we can then in there define a custom property/variable.
The syntax for it is a little weird to get use to, but it should come somewhat fast.

We start by writing "--" followed by the name of our custom variable/property
(which can be called anything, but try to stick to a descriptive name just as with the variables in JavaScript).

Let's say we want to have a variable called "yellow", which contains a yellow color, we would write it like this:
:root {
    --yellow: yellow;
}

If our name has more than one word in it, the convention is to separate each word by a hyphen (-).
So if the example above should be named "yellow color" instead, we would write it like this:
:root {
    --yellow-color: yellow;
}

### USE CUSTOM VARIABLES/PROPERTIES ###
So, once we defined our custom properties/variables, they are ready to use - just like a variable in JavaScript.
The question is just now: How do we do that?
Well, let's say that we want to have the text on the document to be yellow using a custom property/variable, we would write the following:

body {
    background-color: var(--yellow-color);
}

So the syntax is pretty straightforward:
The property name followed by the value (in this case our custom variable/property),
which consists of three parts in the following order:

  - The keyword "var"
  - Then a pair of parentheses
  - Inside of the parentheses is where the name of the custom variable goes.

Note that the value you pass into the parentheses ***must*** match character by character to the name you gave it in the root scope.
Otherwise, it won't work.



### TASK DESCRIPTION ###
1. Go ahead and open up the index_two.html file in your browser.

2. Open up the change_colors_and_border_radius_with_cv.css file.

3. Do as comment in the :root{} tells you to do.

4. First when you've completed step 3 totally, try changing the values of your custom properties/values to see what happens in the browser.

5. Thank me later ;)