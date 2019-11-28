# Problem statement

Implement a data pager class in JavaScript. You **should not use** the ES6 ```class```. A pagination is when you split long arrays of content in a series of small pages.
Your class should accept two parameters:

* ```items[]``` - that is the array you want to control/paginate
* ```pageSize``` - the number of items per page

For example:

``` JavaScript
var pager = new Pager([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11], 3);
```

Add a property ```visibleItems``` to get the currently visible portion of the array.

For example:

``` JavaScript
console.log(pager.visibleItems); // [1,2,3]
```

Add properties for ```currentPage``` - returns the current active page and ```totalPages``` - returns the maximum number of pages.

``` JavaScript
console.log(pager.currentPage); // 1
console.log(pager.totalPages); // 4
```

You need to implement various paging methods like:

* ```nextPage()```
* ```prevPage()```
* ```firstPage()```
* ```lastPage()```
* ```goToPage(page)```

For example:

``` JavaScript
pager.nextPage();
console.log(pager.visibleItems); // [4,5,6]

pager.prevPage();
console.log(pager.visibleItems); // [1,2,3]

pager.lastPage();
console.log(pager.visibleItems); // [10, 11]

pager.firstPage();
console.log(pager.visibleItems); // [1,2,3]

pager.goToPage(3);
console.log(pager.visibleItems); // [7,8,9]
```

## Unit Tests

Write one or more unit tests verifying your solution using a js testing framework by your choice.

## Technologies and Solution

Using JavaScript.
Send us a link to a github repository with the solution.