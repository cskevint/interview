Checkbox Tree
===========

Task 
----

Write a checkbox tree component.

Input
-----

jsonData = [
  { 
    "title": "Arizona",
    "selected": true,
    "children": [
      { "title": "Phoenix", "selected": true },
      { "title": "Tucson", "selected": true }
    ]
  },
  { 
    "title": "California",
    "children": [
      { "title": "Fresno" },
      { "title": "Los Angeles", "selected": true },
      { "title": "Sacramento" },
      { "title": "San Diego" },
      { "title": "San Francisco" },
      { "title": "San Jose" },
    ]
  },
  { 
    "title": "Oregon",
    "children": [
      { "title": "Portland" },
      { "title": "Eugene" }
    ]
  },
  { 
    "title": "Nevada",
    "children": [
      { "title": "Las Vegas" },
      { "title": "Reno" }
    ]
  },
  { 
    "title": "New Mexico",
    "children": [
      { "title": "Albuquerque" },
      { "title": "Las Cruces" },
      { "title": "Santa Fe" }
    ]
  }
]


Output
------

   * [x] Arizona
     * [x] Phoenix
     * [x] Tucson
   * [-] California
     * [ ] Fresno
     * [x] Los Angeles
     * [ ] Sacramento
     * [ ] San Diego
     * [ ] San Francisco
     * [ ] San Jose
   * [ ] Oregon
   * [ ] Nevada
   * [ ] New Mexico


