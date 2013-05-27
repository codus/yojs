yojs
=====

Javascript library for declaring and calling functions and variables using namespaces.

Usage
--------------------

Function definition: 

```javascript
yojs.define("yojs_test", function() {
  //your code goes here
});

yojs.define("yojs_test.comments.new", function() {
  //your code goes here
});
```

Function call:

```javascript
yojs.call("yojs_test");

yojs.call("yojs_test.comments.new");
```

Store objects and values:

```javascript
yojs.set("yojs_test.my_value", 42);
yojs.set("yojs_test.ns2.n3.my_json", { foo: "bar"} );
```

Retrieve stored object and values:

```javascript
var value = yojs.get("yojs_test.my_value");
var json = yojs.get("yojs_test.ns2.n3.my_json");
```

Namespace lookup:

```javascript
yojs.define("my.deep.namespace.teste", function() {
  yojs.call("itworks");
});

yojs.define("my.deep.namespace.itworks", function() {
  console.log("yay");
});

yojs.call("my.deep.namespace.teste") // -> yay
```