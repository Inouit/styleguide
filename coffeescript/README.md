# CoffeeScript guidelines

## Text editor settings
- Tab size: 2 spaces
- Line size: < 120 signs
- Empty last line
- Remove trailing spaces

## Tree structure
```
js/
  |
  |– src/
  |   |– components/                      # Internal components
  |   |   |– getHash.coffee               # Extract a hash from a string
  |   |   |– jquery.backToTop.coffee      # Manage display of *back to top* button
  |   |   |– jquery.fixToTop.coffee       # Fix item to the top of the screen
  |   |   |– jquery.hoverSrc.coffee       # Manage hover state
  |   |   |– jquery.pulldown.coffee       # Manage pulldown items
  |   |   `– jquery.smoothAnchors.coffee  # Smooth scroll on anchors
  |   `– main.coffee                      # Default scripts for the website
  |
  `– vendors/                             # External libraries
```

## Code Sample
```coffeescript
  $ = require 'jquery'

  # Create a Car
  #
  # @example How to park the car
  #   car = new Car( '#garage', 'A4' )
  # @example How to park the car on the first free place
  #   car = new Car( '#garage' )
  #
  modules.exports = class Car

    # @property [String] place number by default
    placeNumber: 'A1'

    # Construct the car
    #
    # @param  [Object] @container where the Car will be parked
    # @param  [String] @placeNumber place number
    # @param [Bool] isThereADeadBodyInTheTruck
    # @event Car.parked is triggered when the car is parked into a garage
    #
    # @return [Car]
    #
    constructor: (@container, @placeNumber, isThereADeadBodyInTheTruck) ->
      @placeNumber ?= @getFirstFreePlace()

      @initialize()
        .binds()

      @el.trigger('Car.created')
      return @

    # ...

    # Manage listerners
    #
    # @event Garage.frontDoorOpened Listen for front door opening
    #
    # @return [Car]
    #
    binds: ->
      $('body').on('Garage.frontDoorOpened', @doStuff)
      return @
```

## Use
- Simple quotes
- Namespaced global variables
- Browserify
- Lint files
- Source map
- [Codo](https://github.com/coffeedoc/codo) comments
- Docblockr still need a fork for coffeescript full compatibilies. You can use [those snippets](https://gist.github.com/Gregcop1/ebb2f4dc64e9f5de2131) in the meantime

## Don't
- Implicit return
- Nested functions without ~parentheses~
- Global variables
- Avoid too many dependencies
