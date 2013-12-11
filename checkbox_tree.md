Checkbox Tree
===========

### Task 

Write a custom checkbox-tree component by hand. 

__The purpose of this test is to determine your ability to create custom components on top of existing, base-functionality JavaScript libraries (e.g. jQuery). You CANNOT use exisiting UI component libraries, plugins or extensions that render a tree with checkbox capabilities.__

### UI Mockup

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

### Component requirements

1.  Only nodes with children can be opened or closed using a plus/minus or right triangle/down triangle (triangle with CSS preferred).
2.  Each node has a checkbox which does not impact closed/open state (checkboxes indicate selection state e.g. for a filter).
3.  If any node or any of its children is initially selected, open it by default at render time. 
4.  [Optional] Provide a UI-only semi-checked state for nodes that have some children checked but not all.

### Input for the Component

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

### Usage

    $("#cities").checkboxTree(jsonData);
    
or
    
    var checkboxTree = new CheckboxTree({
        el: "#cities",
        data: jsonData
    });
    checkboxTree.render();





