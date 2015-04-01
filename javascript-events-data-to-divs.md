# Week 9: Event handlers and loading data into divs 
At the end of this class, you will be able to recreate this Guardian interactive: ["The mind of a heroin addict: the struggle to get clean and stay sober"](http://www.theguardian.com/society/interactive/2014/feb/11/heroin-addiction-recovery-readers-response-interactive).

## Outline
1. [Introduction to jQuery and Underscore](#introduction-to-jquery-and-underscore)
2. [Event handlers](#event-handlers)
3. [Loading data into divs](#loading-data-into-divs)
4. [Combining data into divs with event handlers](#combine-data-into-divs-with-event-handlers)

## Introduction to jQuery and Underscore
jQuery and Underscore are javascript libraries (like the Google Charts library, Leaflet or Bootstrap) that have various built-in functions that make writing cross-browser compliant javascript a little easier.
- [Download](http://jquery.com/) the library or include the CDN at [https://code.jquery.com/](https://code.jquery.com/). 
- _jQuery selectors_: `$("#objectID")` or `$(".objectClass")`
- jQuery selectors allow you to reference and manipulate HTML objects (the DOM - document object model).
- Good jQuery functions to be aware of:
    - `parent()`
    - `find()`
    - `hasClass()`
    - `addClass()`
    - `removeClass()`

## Event Handlers
- Definitions:
	- _Event_: An action that occurs on an HTML page (e.g. a user clicks a button, the page finishes loading, a user hovers over an image)
	- _Object_: Any HTML element (e.g. div, paragraph, headline, image, button)
	- _Action_: Something that happens, generally defined by a function (e.g. open a new window, change an object's color, toggle the visibility of content)
	- _Bind/Attach_: Associate an action after an event occurs (e.g. You may hear people say, 'Bind an event handler to an object')
- An event handler allows you to trigger actions based on events.
- An event handler needs 3 components:
    1. an element to attach the event handler to
    2. an event
    3. an action that gets triggered when the event happens
- Important for later: Event handlers attach events to objects when the handler is loaded into the browser.
- We're going to use jQuery so we don't have to think about [cross-browser compatibility](http://stackoverflow.com/questions/6348494/addeventlistener-vs-onclick).

``` javascript
/* 
An example of an event handler: When a user clicks on a div (#exampleDiv), the background of the div turns red.
Working example: http://jsfiddle.net/w2oa0sbc/1/ 
*/

/* when a user clicks (event) on #exampleDiv (selected object), the function makes the object red (action) */
$('#exampleDiv').on('click', function() {
    $(this).css("background", "red");
});

*/ 
```
- More complicated code example: [http://jsfiddle.net/ej9jhd69/5/](http://jsfiddle.net/ej9jhd69/5/)
- How to Google for built-in events: Google `javascript event <the event you want to look up>`

## Loading data into divs
- We're going to recreate this Guardian interactive: ["The mind of a heroin addict: the struggle to get clean and stay sober"](http://www.theguardian.com/society/interactive/2014/feb/11/heroin-addiction-recovery-readers-response-interactive)
- Three steps
	1. Figure out how to structure your data.
		- Do you see multiples? Make a list.
		- Does each individual multiple have attributes? Make each attribute a key in an object.
		- Write your data as JSON.
	2. Design one example of how your div should look in HTML (this is your "template")
	3. Write a loop and load in data from your data object in javascript.
- Since we don't have time in class to do this all by hand, I've done it before class so we can skip this step for now. Go to [this link](http://www.columbia.edu/~jsk2220/week9-data-divs/guardianHeroinData.js) to get the rest of this data set.
- Let's design the template.
- Put the template in your javascript file.
- Write a loop and replace values with values from JSON.


## Combine data into divs with event handlers
- Complication: Event handlers bind when they are loaded into the browser (generally when the page loads). So if your element isn't on your page by the time that happens, your event handler doesn't bind to anything.
- Solution: Let's add the event handler and bind it to the object when we create the object.