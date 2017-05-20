*Please explain the difference between the following jQuery functions. What impact has or will this have on code you’ve written?*

1. $(“.todo-item”).on(“click”, function(e){ console.log(e) });

2. $(document).on(“click”, “.todo-item”, function(e){ console.log(e) });

By setting the event handler directly on the element, as in example 1, it is bound directly to the element and will be triggered if anything already existing with `.todo-item` is clicked. If the element was added after the time of binding, it won't execute. By binding the event handler to the document, which we know is definitely in the DOM, we are able to apply this code to `.todo-item` elements that didn't exist in the DOM yet when it was binding. 