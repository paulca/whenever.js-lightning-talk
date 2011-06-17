!SLIDE small
# Chaining #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .given('The Text is "Click Me!"')
        .and('one and one make two')
      .then ('Change the text to "Clicked!"')

## conditions.js ##
    @@@ javascript
    whenever.conditions.add({
      'The Text is "Click Me!"': function(){
        return $(this).text() === 'Click Me!'
      },
      'one and one make two': function(){
        return 1+1 === 2
      }
    })

!SLIDE smaller
# Chaining #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .given('The Text is "Click Me!"')
        .and('one and one make two')
        .and('two and two make five')
      .then ('Change the text to "Clicked!"')

## conditions.js ##
    @@@ javascript
    whenever.conditions.add({
      'The Text is "Click Me!"': function(){
        return $(this).text() === 'Click Me!'
      },
      'one and one make two': function(){
        return 1+1 === 2
      },
      'two and two make five': function(){
        return 2+2 === 5
      }
    })

!SLIDE
# Chaining #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .given('The Text is "Click Me!"')
        .and('one and one make two')
      .then ('Change the text to "Clicked!"')
        .and('Change your haircut')

!SLIDE
# Chaining #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .given('The Text is "Click Me!"')
        .and('one and one make two')
      .then ('Change the text to "Clicked!"')
        .and('Change your haircut')
        .and('Change your job')

!SLIDE
# Chaining #
## app.js ##
    @@@ javascript
    whenever("Click Me!")
      .is   ('clicked')
      .given('The Text is "Click Me!"')
        .and('one and one make two')
      .then ('Change the text to "Clicked!"')
        .and('Change your haircut')
        .and('Change your job')
        .and('Change the world')