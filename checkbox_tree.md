Checkbox Tree
===========

Task 
----

Write a custom checkbox-tree component by hand. 

__The purpose of this test is to determine your ability to create custom components on top of external base-functionality JavaScript libraries (e.g. jQuery). You CANNOT use exisiting UI component libraries, plugins or extensions that render a tree with checkbox capabilities.__

UI Mockup
---------

    + [x] Arizona
      * [x] Phoenix
      * [x] Tucson
    + [-] California
      * [ ] Fresno
      * [x] Los Angeles
      * [ ] Sacramento
      * [ ] San Diego
      * [ ] San Francisco
      * [ ] San Jose
    - [ ] Oregon
    - [ ] Nevada
    - [ ] New Mexico
    $.ajax

### Data Load and Transformation

1. Perform a JSONP ajax call like so:    
<pre>$.ajax({
        url: "https://raw.github.com/cskevint/interview/master/checkbox_tree.json",
        dataType: "jsonp"   
});</pre>

2. This will call a __window.data__ function with the result JSON string as the argument. You will need to parse it to look like the structure below as input for the component.


### Component requirements:

1.  Only nodes with children can be opened or closed using a plus/minus or right triangle/down triangle.
2.  Each node has a checkbox which does not impact closed/open state (checkboxes indicate selection state).
3.  If any node or any of its children is initially selected, open it by default. 
4.  [Optional] Provide a UI-only semi-checked state for nodes that have some children checked but not all.
5.  [Optional] Make it pretty.

### Code requirements

1.  You can use base JavaScript libraries such as jQuery, underscore.js, Backbone.js, etc.
2.  HTML markup should be written through JavaScript either as templates or by creating DOM nodes.
3.  CSS should be contained in its own file which could be included in any application page.
4.  Component constructor takes in JSON data (which can be provided as a variable for the purposes of this test).
5.  Provide a public API that retrieves the selection state of the component in JSON format (semi-checked is false).
6.  You cannot change the structure of the JSON data -- imagine it is coming from the server.
7.  Submit code in a [JSFiddle](http://jsfiddle.net) (preferable) or a [Gist](http://gist.github.com/).

Input for the Component
-----------------------

    jsonData = [
        {
            "name": "Arizona",
            "selected": true,
            "children": [
                { "name": "Phoenix", "selected": true },
                { "name": "Tucson", "selected": true }
            ]
        },
        {
            "name": "California",
            "children": [
                { "name": "Fresno" },
                { "name": "Los Angeles", "selected": true },
                { "name": "Sacramento" },
                { "name": "San Diego" },
                { "name": "San Francisco" },
                { "name": "San Jose" },
            ]
        },
        {
            "name": "Oregon",
            "children": [
                { "name": "Portland" },
                { "name": "Eugene" }
            ]
        },
        {
            "name": "Nevada",
            "children": [
                { "name": "Las Vegas" },
                { "name": "Reno" }
            ]
        },
        {
            "name": "New Mexico",
            "children": [
                { "name": "Albuquerque" },
                { "name": "Las Cruces" },
                { "name": "Santa Fe" }
            ]
        }
    ];

Usage
-----

    $("#cities").checkboxTree(jsonData);
    
or
    
    var checkboxTree = new CheckboxTree({
        el: "#cities",
        data: jsonData
    });
    checkboxTree.render();





