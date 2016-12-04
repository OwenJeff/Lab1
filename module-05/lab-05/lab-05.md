# Lab 05: Using JavaScript Functions

To begin, first open the *lab-05-data/index.html* file within the Working Files in Brackets.  Inspect the contents of this file, and then open the file in your web browser using the Live Preview (and, as usual, open your web developer toolbar/Console as well). 

You'll notice that an HTML UI button element has been added to the page, and has an id attribute of `map-cities` and display content of "Map Cities" (`<button id='map-cities'>Map Cities</button>`).

The JavaScript contains some code that will listen for a user click event on this button. When the user clicks, the contents of the addEventListener's function (known as a "callback function") are executed. Specifically, a [JavaScript prompt function](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt) prompts the user to enter some text, and then assigns the string that's entered to the variable `units`. The code then logs that value of `units` to the console. You should test this within your browser's Console.

```javascript
button.addEventListener("click", function() {
         
        var units = prompt('Enter the units for calculating density', 'Enter "miles" or "km"');
        
        console.log(units); 
        
    });// addEventListener callback function ends here
```

Test this code by typing strings into the prompt and looking for them in the browser console.

The goal of this task is to finish writing a script that:

1. after prompting the user to enter either 'miles' or 'km' and storing this result in a variable
2. calls a function to make the map and sends this variable as an argument
3. uses a looping structure to populate the map with markers while building a popup that displays the name of each city and its population density

We'll be encapsulating our code within **2 functions** we'll write to achieve this. Follow these directions to continue, but first study the example code supplied within the *lab-05-data/example.html* and see the accompanying video for lesson/lab 05.

1. Where indicated at the top of your script (below the code provided that creates the map and adds the tiles to the map), build 4 array structures to hold the names of 3 different cities of your choosing, their coordinates (lat/lng), their current population, and the area of each city. These will be similar to the arrays used in Lab 04; the cityCoords array will be a nested array. These arrays contain your data used for the map.

2. Within the `addEventListener()` callback function, replace the `console.log()` statement with a call to a function named `mapCities()` and pass the `units` variable as an argument. We wish to wait until the user has entered either 'miles' or 'km' before executing the code within the `mapCities()` function.

3. Immediately write a new function named `mapCities()` where the comments indicate. This function will need to accept the `units` variable as a parameter. Within this function's body, write code that loops through the `cities` array. Within this loop, you can access each of the city's  population and area values (i.e., using `cities[i]` syntax, see Lab 04). Within the loop, call a second function named `calcPopDensity()` and pass the population, the area, and the units (which will be either 'km' or 'miles') as arguments. The return value from this function will be assigned to a variable named `density` (similar to how the `prompt()` function assigns the return value to the variable `units` above). 

4. Now write the new function named `calcPopDensity()` where indicated (outside of the `mapCities` function's body!). This function needs to accept 3 values as parameters: a single city's population, its area, and the variable `units` designated within the `mapCities` function (i.e., 'miles' or 'units'). Write code within the function's body that accomplishes:

    a. First determine whether the units are in miles or kilometers using conditional logic, and then 
    
    b. Calculate the population density using the population and area values before returning the result to the caller (i.e., this value will be assigned to the `density` variable within the `mapCities` function). Your code within these conditional (if/else) statement bodies will need to mathematically convert the miles to kilometers if the value of `units` is changed to be 'km'.
    
    c. Return the calculated density value

5. Once the  `calcPopDensity()` is complete, save and test your code to ensure there are no errors. You may wish to write a `console.log()` statement beneath the line in the `mapCities()` function logging the returned value of the density to ensure it is valid.

6. Once you have the density value available to you within the `mapCities()` function loop, you can then build up the markers and popups in a similar fashion as in Lab 04. There will be one variable named `popup` which is assigned a concatenation of string values. These need to include the name of the city and the density of the city. The coordinates will be used to place each marker in its correct position.

7. Finally, change the `h1` and `h2` tags to update your web document with title and subtitle, and edit the text at the bottom of the page (e.g., author and meta information). Feel free to customize and personalize the look and feel of your page (using CSS rules).

Be sure that your code is clean and uniformly indented.

Additionally, include the *lesson-05-data/index.html* file with the examples demonstrated within the lesson saved in the file.

**Final challenge:** Note how if the user enters information incorrectly (a value of something other than 'miles' or 'km' for the unit), the script essentially breaks and the page must be reloaded. How would you go about catching these errors and again prompt the user to enter the correct information? Hint: consider using a looping mechanism and read about the [do ... while statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/do...while).

Sync your final solutions with your remote repository and provide a link within Canvas by the due date.
