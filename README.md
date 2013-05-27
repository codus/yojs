Codus
=====

Javascript library for declaring and calling functions and variables using namespaces.

Usage
--------------------

Function definition: 

cJS.define("cjs_test", function() {
  //your code goes here
});

cJS.define("cjs_test.comments.new", function() {
  //your code goes here
});

Function call:

cJS.call("cjs_test");

cJS.call("cjs_test.comments.new");

Store objects and values:

cJS.set("cjs_test.my_value", 42);
cJS.set("cjs_test.ns2.n3.my_json", { foo: "bar"} );

Retrieve stored object and values:

var value = cJS.get("cjs_test.my_value");
var json = cJS.get("cjs_test.ns2.n3.my_json");
