!SLIDE

# Code Examples!

!SLIDE title-slide

# Comments

## `ruby`
        #
        begin=; end=

## `smalltalk`
        ""

!SLIDE title-slide

# Characters are not Strings

## `ruby`
        'a'.class  # => String

## `smalltalk`
        'a' class  "# => String"
        $a class   "# => Character"

!SLIDE title-slide

# Quote Escaping in Strings

## `ruby`
        'hello "world"'
        "hello 'world'"
        "hello \"world\""

## `smalltalk`
        'Hello ''world'''

!SLIDE title-slide

# Symbols

## `ruby`
        :foo_bar

## `smalltalk`
        #fooBar

!SLIDE title-slide

# Arrays

## `ruby`
        [0, 1, 2]

## `smalltalk`
        #(0 1 2)             "# literal array"
        {0. 1. 2}            "# dynamic array"
        #(0 1 2) = {0. 1. 2} "# => true"

!SLIDE title-slide

# Meaning of Binary Messages are not "hard\-wired"
# They are all treated the same

## `ruby`
        3 + 4 * 5  # => 23

## `smalltalk`
        3 + 4 * 5  "# => 35"

!SLIDE small title-slide

# Cascade uses semi\-colons

## `ruby`
        a = 1; b = 2

## `smalltalk`
        game := Game new 
                     board: newBoard;
                     ui: newUi;
                     playerX: newPlayerX;
                     playerO: newPlayerO.

# use `.` to terminate statements

!SLIDE small title-slide

# Booleans receive messages

## `smalltalk`
        (1 + 1 = 2)
          ifTrue: [Transcript show: 'AWESOME']
          ifFalse: [Transcript show: 'NOT SO AWESOME'].

!SLIDE title-slide

# Comparison syntax

## `smalltalk`
        =   "# equality comparison"
        ==  "# identity comparison"
        ~=  "# inequality comparison"
        ~~  "# not identical comparison"

!SLIDE title-slide

# Blocks

## `smalltalk`
        block := [Transcript show: 'I''m a block!'].
        block value.  "# => I'm a block!"

### Common keyword messages with block arguments:
        collect:
        select:
        reject:
        detect:
        inject:into:

!SLIDE small title-slide

# Blocks receive other messages

## `smalltalk`
        | flag |

        flag := true.
        [flag] whileTrue: [ flag := false. ].

        flag := false.
        [flag] whileFalse: [ flag := true. ].

!SLIDE small title-slide

# Switch Functionality

## `smalltalk`
        switch := Dictionary new.
        switch at: $A put: [Transcript show: 'Case A'; cr].
        switch at: $B put: [Transcript show: 'Case B'; cr].
        switch at: $C put: [Transcript show: 'Case C'; cr].

        result := (switch at: $B) value.  "# => Case B"

!SLIDE smaller title-slide

# Class Example

## `smalltalk`
        Object subclass: Person [
            | name age |
            Person class >> name: aString age: anInteger [
                ^self new name: aString; age: anInteger; yourself
            ]

            name [ ^name ]
            name: aString [ name := aString ]
            age [ ^age ]
            age: anInteger [ age := anInteger ]

            printOn: aStream [
                aStream << ('%1 (%2)' % {name. age})
            ]
        ]

!SLIDE title-slide

## `smalltalk`
        | name age |  "# declares variables"

### *Type of variable depends where variables are declared*

!SLIDE small title-slide

# To create a Person object

## `smalltalk`
        |billy|
        billy := Person name: 'Charley' age: 12.
        
        "# => 'Charley (12)''"

!SLIDE title-slide

# Debugging

## `smalltalk`
        respondsTo:
        inspect
        explore
        halt
