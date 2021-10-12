![jQueryWeatherApp](https://user-images.githubusercontent.com/63736914/136951474-81b3b784-cde3-4293-8513-6818421a051c.png)
# weather-app-jQuery (Walkthrough)

  ## The function api_call:
  1. Grabs user location by calling the jQuery .val()
     method (user input constant).
  2. API_KEY provided by openweathermap.
  3. The url we want to make the request to as `template literal`.
     We are injecting the location constant that gets updated by what the user 
     types.
  4. We start off by making a check: (if) the "location" exists (value of the user input),
     only then we want to go ahead and make a request to the url.
  5. If the "location" does not exist (else) we call right at the end
      the .show() method on the "error" to display it and then we .hide()
      the weather data in case is there.
  6. In the block of code we use AJAX to make the web request to the const "url"
     which is specified and inside we check if the request was succesful
     (success method) and then we grab all the properties that
     we want to extract from the API in order to display the data.
  7. The Weather constant will determine what kind of icon will be displayed.
     We make this data widget visible by calling the jQuery method .show()
     then we create h3, p, img and button markup elements to go in our div in the main
     index.html.
  8. We create a constant that contains the value of "details" button.
     The CSS class ".weather-details-button" is associated.
  9. Up to here this is still calling the API function, 
     we need to wait to call this function and we do that by setting the jQuery method onto the searchButton.click()
     and we prevent the default behaviour with the preventDefault()
     method on our event object (because we are submitting a form we don't want refresh the page).
  10. Finally we call the api_call() function when the user clicks this button.
