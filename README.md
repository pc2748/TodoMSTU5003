# TINKER - Javascript Part II

- See repository: https://github.com/jmk2142/TodoMSTU5003
- See demonstration: https://jmk2142.github.io/TodoMSTU5003
- Tinker Markdown (Prettier): https://hackmd.io/s/SkY3UWsMb

For this week, the actual Markdown file is not available via Github Gists. I have included it within this week's Tinker repository along with the rest of the code. It is called `README.md`. You might want to `IMPORT` the markdown into hackmd.io to use that tool (recommended.)

To get access to this code, and the actual Markdown to play with, you can use Github to CLONE the repository using the Github GUI Client. You can get the idea of what repositories are in my Youtube Video:

## Github: How to clone my repository

You'll want to start with the video overview:
https://youtu.be/QOXhN90d9Mk?list=PLn93-yl6k7zUkSFNI8MQqmIVn017z8vKO

Since you want to copy MY repository, once you have the Github GUI Client installed - you can do so with one click of a button. Just click on the Clone or download option, then **Open in Desktop** and that will automatically open it up in the Git GUI. (See Below)

![Clone thorugh Github](https://i.imgur.com/onzsWMy.png)

Keep in mind that since you are cloning my repository, you will only be able to commit changes to your local computer. You will not be able to _sync_ or _push_ changes to my Github repository - for obvious security reasons. (You wouldn't want just anyone to change YOUR code.)

If you would like to use Github for your work in progress, what you can do is **_FORK_** my repository first. (See _FORK_ button under account picture.) This will create a copy of this repository under your account name in Github. You can clone YOUR version of this to your local computer, then commit and push to your account to your heart's content. :smiley_cat:

---

## Devtools
You will also want to watch this video on the `console` as we will be using it extensively to Tinker this week.

https://youtu.be/GAqOggzH_GE?list=PLn93-yl6k7zUkSFNI8MQqmIVn017z8vKO

:::danger
**NOTICE**

I'm still in the process of creating a video on how to use the debugging tool.

_Coming Soon !_
:::


## Tinker GIST: TODOS

> Good bye, "Hello World!"

`Hello World` is probably the most common introductory program around as it's so simple.

```javascript=
alert("Hello World!");

// Or alternatively...

console.log("Hello World!");
```

Unfortunately, it's not very useful. It doesn't really show the range of different programming concepts and to be quite frank, it's boring. Many beginners like us are interested in creating interactive applications and this requires a range of programming concepts.

1. HTML Elements
2. CSS
3. Variables
4. Operators
5. Functions
6. Control Statements
7. Events
8. Data Structures + Data (e.g. Arrays, Objects, Booleans, Numbers, Strings)

And you really cant get a sense of how these things work together with a 1 line program like `Hello World!`.

### Enter TODOS

Some clever programmer realized this and probably thought:

> What's the simplest, _real_ program I can build that will incorporate all the important aspects of a basic interactive program?

And the **TODOS** or **TODO LIST** program was born.

The beauty of TODOS is that it has everything in a pretty simple package. It can be solved using a variety of different strategies and can be created to be _simpler_ or _more sophsiticated_ depending on ones needs. It tends to now be the defacto standard for demonstrating a full interactive application.

Beginners AND advanced students alike build TODO apps as they learn new things. For example, our TODOS Tinker is designed to demonstrate the base JS concepts with a few _stretch_ challenges embedded in it. In my regular practice, when I have to learn a new library or framework, I will probably start by viewing an existing TODO app built with that specific library to see how that library works. Sort of like how you might compare a basic HTML page with a Bootstrap page (of the same content) to be able to compare and contrast the two. If you're interested, you can briefly look at [this page](http://todomvc.com/) which is an archive of the TODO application built in various different frameworks.

And this is where I am hoping to take this class, the culmination of all the things we've been working towards - to understanding this first, real, interactive program and hopefully - you can apply some of these concepts in your own works.


## Tinker Tasks

In this tinker, were going to:

1. Review prior concepts in this new context:
    - Variables, functions, events, and arrays
2. Observe, analyze, and study new concepts:
    - Control statements (E.g. `if`, `for`)
    - Logical operators (E.g. `===`,`&&`, `||`,`<`,`<=`,`>`,`>=`, etc.)
    - Objects (and `array` of `objects`)
3. Learn how to use more developer tools to study JS code
    - Source (i.e. debugger)
    - Console (i.e. `console.log`, `console.dir`)

We will continue to observe, analyze and think about this program in terms of:

> What is the STATE?
> What is the SEQUENCE?
> What is the CAUSALITY?



### Part 0: Conceptual Program Overview

Play with the program and observe how it reacts to user interactions.

- _Without_ talking about it in _programming terms_ explain the user observable steps/process of the following three interactions and how the program responds.
  - Adding a todo
  - Completing a todo
  - Removing a todo(s)

  Be specific but imagine you are talking to a _non-programmer_. Think about this in terms of observable actions and reactions.
  > User puts toast in the toaster. Sets the length of the timer. Pushes the lever to start the toaster. The toaster pops out the toast after the time is completed and goes "DING".
- For each of the interactions above write in _pseudocode_ the steps of how the program for that interaction unfold and results. Pseudocode is semi-formal structure to write out the gist of how your program would work. It uses some keywords but is largely language agnostic. There isn't a single correct way to do it but the following are some rules that can help.
  - RULES:
    - One statement per line
    - CAPITALIZE initial _keywords_
      - READ, WRITE, IF, ELSE, REPEAT, UNTIL, AND, OR
    - Indent to show hierarchy and groups of operation
    - Keep statements language independent

  ```markdown=
  # Making toast for a big family
  READ loaf of bread
  READ slide of loaf
    Put slice in toaster
      WRITE time to toast
      Start the toaster
        Cook the toast
          READ time
          WRITE time by one second less
        REPEAT UNTIL time is zero
    Remove toast
  REPEAT for all slices in loaf

  # Serving toast
  WRITE number of slices total
  READ number of family members
  READ toastiness
  IF toast is burnt AND (total slices >= number of family members)
    throw away toast
    decrement slices total
  ELSE
    serve toast to family member
  ```
- Using your pseudocode, identify the function(s) in the actual JS code that relate to your pseudocode.
  - Compare and contrast your pseudocode with the actual code.
  - Explain what similarities and differences you noticed about the instructions / steps / processes in the code vs. your psuedocode.

- Manipulate different parts of the code as you see fit. Why did you decide to manipulate that part? What happened? (More structured tinkering to follow.)


### Part 1: Variables, Functions, Arrays, and Events

- Explain the `data` variable.
  - What does this data (and the data inside) represent conceptually?
  - If I wanted to access the second object, how would I do that in code?
  - If I wanted to access the `done` property of the first object, how would I do that?

- Look through the rest of the code where this `data` array is used. When the user does things, am I manipulating the visual display and updating the data to reflect those changes? Or am I manipulating the data and updating the visual display to reflect those changes?
  - Is this what you would have thought of?
  - What might be the significance of this program design decision?

- What do these lines in my code do?
    ```javascript=
    var todosEl = document.querySelector('#todos');
    var inputEl = document.querySelector('input');
    var completedEl = document.querySelector('#counter');
    ```
- Why declare these (see above) variables at the Global scope instead of in the functions?
  - Or not at all... (E.g. `document.querySelector('#todos');`)

- The `toggleComplete` function has an event parameter. Inside the function I access `event.currentTarget`. What is the difference between `event.currentTarget` and `event.target` which we used previously?
  - Hint 1: You can add a `console.log(event)` etc. inside that function to test the value of `event.target` and `event.currentTarget`.
  - Hint 2: When testing, click on a todo to "complete" it. Click on two areas: the `li` as well as the `i` (font icon) element to see the differences.
  - Hint 3: You can pass multiple arguments to `console.log()`. I often pass two: first a string label, second the thing I want to log. This will basically make the logs easier to identify if you use `console.log()` a lot.

  ```javascript=
  console.log("SOME LABEL: ", dataToLog);
  ```
- In the `toggleComplete` function, there is a `event.currentTarget.id`. Is that `id` the same thing as the id property in my todo objects in the `data` array?
  - Explain.
- What does `!something` mean? (The exclamation mark) and how is it used in this code when we `toggleComplete`?

- Try calling some of the functions directly from the console. Some will work. Some won't.
  - Explain what you find.

- Look at the function declarations in the `todos.js` file.
	- _Where_ is each function being called?
	- _When_ is each function, actually called?
	- What parameter(s) does that function have?
	- What is the argument that is passed into the function when it is called?

- Use the console (in Chrome devtools) to `console.log()` and `console.dir()` the following. What is the difference between `console.log` and `console.dir` and why is `console.dir` kind of more useful for looking at some kinds of data?
    ```javascript=
    console.log(data);
    console.log(todosEl);

    console.dir(data);
    console.dir(todosEl);
    ```


### Part 2: Objects and Arrays of Objects

- Manipulate the different _properties_ of the _objects_ inside the `data` array.
  - Change all todo objects' `done` property to `true`.
  - Change some of the task values.
  - Run your code and explain how this changes what you see and why.

- `console.dir()` the `data` array. Goto the console and _OPEN_ the `> Array(3)` text by clicking on it. Go deeper by opening up the nested objects. Analyze what you see. Then add a new todo through the user interface. `console.dir()` the `data` array again and investigate the insides.
  - What is the difference between `data` before and after adding a new todo?

- Run the following code:
    ```javascript=
    data.push({
      done: true,
      task: "Goto Aikido Lessons",
      id: getTimeStamp()
    });
    console.dir(data);
    ```
  - What did the code above do?
  - Does our page reflect the changes made? Why or why not? Prove it.
  - Does order matter in `Objects`?

- What is the difference between `Object` keys (E.g. `done`, `task`, `id`) and `Array` indices (E.g. `0`, `1`, `2`)?
  - How are they similar?
  ```javascript=
  var myAry = [123, "Code", true];
  var myObj = {
    id: 123,
    task: "Code",
    done: true
  }
  console.log(myAry[1]);
  console.log(myObj["task"]);
  console.log(myObj.task);
  ```

- Compare the following in the console:
  ```javascript=
  var element = document.querySelector('ul');
  var author = { first: "Mark", last: "Twain" }

  var example = {
    theAnswer: 42,
    student: true,
    hobby: "Fishing",
    sayHello: function(){
      alert("Hello");
    },
    favNums: [1,2,3],
    favAuthor: author
  };

  console.dir(example);
  console.dir(el);
  ```
  - What is an `element` really?
  - How does our `element` relate in terms of similarities and differences to `example`?
  - If I wanted to call the function in the `example` object, how would I do that? Prove it.

- Try the following code in the console. How does dot notation and bracket notation differ and why would you want to use one or the other?
  ```javascript=
  var x = "username";
  var user = {
    username: "happyCat"
  }
  console.log(user.username);
  console.log(user["username"]);
  console.log(user[x]);
  console.log(user.x);
  ```
- Identify various areas where the `.` object notation is used and explain the thing on the left side of the `.` and the thing on the right side of the `.`
  - E.g. `document.querySelector()` `document` is... `querySelector` is...
  - HINT: There are MANY choices here.

- In two areas of my code, I use what is called a `filter` function. It's a function that arrays can use like `list.pop()`, `list.push()`.
  - How does a filter function work?
  - What is the significance of the function argument that is passed INTO the filter parameters?
  - With regard to the function that is passed into the filter as an argument, that function must `return` a boolean or evaluate to a boolean. What is the purpose of this?
  - What does the _filter function_ return?
    E.g. `var x = list.filter(...); // What was returned to x?`
    - CAUTION: NOT the function argument that goes into the filter.
    - HINT: If you don't know, can you use console to "test" an idea out?
  - Does filtering an array _change_ the original array?

### Part 3 Control Structures

- I use the `if` statement in several places in this code. Explain why a conditional is necessary in:
  - `updateTodoItems`
  - `updateRemoveButton`
  - `onEnterKey`
  - `validateTask`
  - `addTodoItem`
  - `getTodoData`
  - HINT: You might want to `console.log` the boolean condition where you see the `if` statements to understand what condition we are evaluating.
  ```javascript=
  if (booleanCondition) {
    ...
  }
  console.log(booleanCondition);
  ```
  - Comment on how the boolean condition works as there are many different examples.

- In this code, there are two kinds of `for` loops. The more traditional that looks like:

    ```javascript=
    for (var i=0; i < list.length; i++) {
      // CODE
    }
    ```
    and a `for of` loop that looks like:
    ```javascript=
    for (item of list) {
      // CODE
    }
    ```
  - How does a `for of` loop work?
    - What does the `item` represent? (It can be named anything: `x`, `item`, `thing` etc.)
  - Why are `for of` loops convenient compared to the traditional `for`?
  - For what purpose(s) do I employ a `for` or `for of` loop in this program?
  - On Facebook or Pinterest, or Twitter, how does a loop through data relate to the display of content?

### Part 3 Specific Routines

- Take a look at the `updateTodoItems`. Comment it out and replace it with this alternate, but functionally identical version. How does this function work and how do they relate / differ?
```javscript=
function updateTodoItems() {
  todosEl.innerHTML = "";

  if (!data.length) {
    var liElement = document.createElement('li');
    liElement.innerText = "Nothing todo...";
    todosEl.appendChild(liElement);
  } else {

    for (todo of data) {
      var liElement = document.createElement('li');
      var iElement = document.createElement('i');

      liElement.id = todo.id;
      liElement.onclick = toggleComplete;

      if (todo.done) {
        liElement.className = "complete";
        iElement.className = "fa fa-check-circle-o";
      } else {
        iElement.className = "fa fa-circle-o";
      }

      liElement.appendChild(iElement);
      liElement.innerText = todo.task;

      todosEl.appendChild(liElement);
    }
  }

  updateRemoveBtn();
}
```

- Take a look at the helper function `getTimeStamp`. This function will return a number, in milliseconds, the current time stamp since January 1, 1970.
  - I call this when I create new todo items, what are some ideas as to why I might be using a timestamp for todo `ids`?

- Take a look at the incomplete functions `markAllComplete` and `updateItemsLeft`.
  - Can you complete these and add the functionality to this app?

### Part 4 Debugging, Tools

Using the Chrome debugger (source) tool create breakpoints and watch the program execute line by line, part by part. Experience how this tool can give you insight into your program's _STATE_, _SEQUENCE_, _CAUSALITY_.

#### Chrome Debugger

- Set breakpoints at the following locations of your program
  - `function initializeTodos`
  - `function onEnterKey`
  - `function addTodoItem`
  - `function toggleComplete`

- Use the `Step over the next function call` feature to watch how the program pauses during the _SEQUENCE_ of its routines.
- Use the `Step into the next function call` feature to watch how the program pauses during the _SEQUENCE_ of its routines.
  - What is the difference between `Step over` and `Step into` and how does this help you understand programs?
- Use `Step into` until you've reached the line `var inputEl = document.querySelector('input');`. Should be highlighted in blue.
  - Highlight the variable `todosEl` on the line before it and `right click` on it. Select _Evaluate in console_.
    - What does the console print?

  - Highlight the variable `inputEl` on this highlighted blue line.
    - Why does the console say `inputEl` is undefined?
    - When you step through your code, does the blue line represent code that is about to be executed or code that has already executed? How do you know?
    - What do you predict would be the console value of the variable `completedEl` on the next line if you _Evaluate to console_ at this point?
- Watch how debugger annotates your source code with the updated _state_ of different variables as your program progresses.
  - How does the debugger behave when you enter a loop in your program?
  - How does the debugger behave when you reach the a `filter` function call?
  - What does filter do and how does it work?


### Part X: Putting all together

**Explain the program line by line with sufficient details, part by part.**
:::success
- Line by line
  - Part by part
- Be sure to copy blocks of code into this markdown using code formatting/fences as references to your explanations.
- For repetitive code, you can explain how a line works then summarize how it would work for the rest.
:::
**Make it yours (group's)**
:::success
- Try to extend this program to do something cool, as a group, your own original idea(s).
	- What is something that a Todo list or todo list user might benefit from?
:::
