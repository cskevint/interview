Checkbox Tree
===========

Task 
----

Write a custom checkbox-tree component. 

### Component requirements:

1.  Only nodes with children can be opened or closed using a plus/minus or right triangle/down triangle.
2.  Each node has a checkbox which does not impact closed/open state (checkboxes indicate selection state).
3.  If any node is initially selected, open it by default. 
4.  [Optional] Provide a UI-only semi-checked state for nodes that have some children checked but not all.
5.  [Optional] Make it pretty.

### Code requirements

1.  You can use non-UI component JavaScript libraries such as jQuery, underscore.js, Backbone.js, etc.
2.  HTML markup should be written through JavaScript either as templates or by creating DOM nodes.
3.  CSS should be contained in its own file which could be included in any application page.
4.  Component constructor takes in JSON data (which can be provided as a variable for the purposes of this test).
5.  Provide a public API that retrieves the selection state of the component in JSON format (semi-checked is false). 
6.  Submit code in a [JSFiddle](http://jsfiddle.net) (preferable) or a [Gist](http://gist.github.com/).

Input Data
----------

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


Output UI
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


