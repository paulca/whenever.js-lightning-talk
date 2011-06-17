!SLIDE
# Basics #
# app.js #
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .then ('Change the text to "Clicked!"')

!SLIDE
# Basics #
# app.js #
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .then ('Change the text to "Clicked!"')

# definitions.js #
    @@@ javascript
    whenever.definitions.add({
      "Click Me!": 'a#click-me'
    })

!SLIDE smaller
# Basics #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .then ('Change the text to "Clicked!"')

## definitions.js ##
    @@@ javascript
    whenever.definitions.add({
      "Click Me!": 'a#click-me'
    })

## actions.js ##
    @@@ javascript
    whenever.actions.add({
      'Change the text to "Clicked!"': function(){
        $(this).text('Clicked!')
      }
    })

!SLIDE smaller
# Basics #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .then ('Change the text to "Clicked!"')

## definitions.js ##
    @@@ javascript
    whenever.definitions.add({
      "Click Me!": 'a#click-me'
    })

## actions.js ##
    @@@ javascript
    whenever.actions.add({
      'Change the text to "([^"]*)"': function(value){
        $(this).text(value)
      }
    })