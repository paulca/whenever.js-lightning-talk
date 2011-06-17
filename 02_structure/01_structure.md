!SLIDE small
# Structure #
    jquery.js
    whenever.js
    (definitions.js)
    (actions.js)
    (conditions.js)
    app.js

!SLIDE small
# Size #
    3.4K unzipped
    1.5K minified
    665B gzipped

!SLIDE
# Cucumber #
    @@@ cucumber
    When "Click Me" is clicked
    Then Change the text to "Clicked!"

!SLIDE
# jQuery #
    @@@ javascript
    jQuery('a#click-me').click(function(){
      $(this).text('Clicked!)
    })

!SLIDE
# Coffeescript #
    @@@ javascript
    jQuery('a#click-me').click ->
      $(@).text 'Clicked!

!SLIDE
# whenever.js #
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .then ('Change the text to "Clicked!"')