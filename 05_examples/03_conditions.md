!SLIDE
# Conditions #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .given('The Text is "Click Me!"')
      .then ('Change the text to "Clicked!"')

!SLIDE
# Conditions #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .given('The Text is "Click Me!"')
      .then ('Change the text to "Clicked!"')

## conditions.js ##
    @@@ javascript
    whenever.conditions.add({
      'The Text is "Click Me!"': function(){
        return $(this).text() === 'Click Me!'
      }
    })

!SLIDE small
# Conditions #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .given('The Text is "([^"]*)"')
      .then ('Change the text to "Clicked!"')

## conditions.js ##
    @@@ javascript
    whenever.conditions.add({
      'The Text is "Click Me!"': function(value){
        return $(this).text() === value
      }
    })