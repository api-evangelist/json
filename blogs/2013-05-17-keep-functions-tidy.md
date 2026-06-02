---
title: Keep Functions Tidy
url: http://json.com/2013/05/17/keep-functions-tidy.html
date: '2013-05-17'
author: ''
feed_url: https://json.com/atom.xml
---
When you want to keep your functions out of the global namespace, use JSON.  A common development pattern for this is placing functions inside an object looks like this: var nameSpace = { "myFunc" : function ( x , y ){ return x + y ; }, "otherFunc" : function ( x , y , z ){ return this . myFunc ( x , y ) * z ; } } Now you can access your functions the same way you access any other object property.  In this case, the functions are referred to as “methods”. console . log ( nameSpace . myFunc ( 1 , 2 ) ); // returns 3 Another advantage you have of declaring functions in an object literal is
gaining access to the this variable within each method.  In the example
above, this refers to nameSpace object.  It can be referred to easily in this manner without declaring any functions in the global namespace.  Handy indeed.
