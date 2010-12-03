!SLIDE

# Code Examples!

!SLIDE bullets

# Comments

* `# ruby`
* `#`
* `begin=; end=`

* `"# smalltalk"`
* `""`

!SLIDE smbullets

# Characters are not Strings

* `# ruby`
* `'a'.class  # => String`

* `"# smalltalk"`
* `'a' class  "# => String"`
* `$a class  "# => Character"`

!SLIDE bullets

# Quote Escaping in Strings

* `# ruby`
* `'Hello "world"'`
* `"Hello 'world'"`
* `"Hello \"world\""`

* `"# smalltalk"`
* `'Hello ''world'''`

!SLIDE bullets

# Symbols

* `# ruby`
* `:foo_bar`

* `"# smalltalk"`
* `#fooBar`

!SLIDE bullets

# Arrays

* `# ruby`
* `[0, 1, 2]`

* `"# smalltalk"`
* `#(0 1 2)  "# literal array"`
* `{0 . 1 . 2} "# dynamic array"`

!SLIDE bullets

* `~=  "# !="`
* `^  "# return"`
* `&  "# AND"`
* `|  "# OR"`

!SLIDE bullets

## Meaning of Binary Messages are not "hard\-wired"
## They are all treated the same

* `# ruby`
* `3 + 4 * 5  # => 23`

* `"# smalltalk"`
* `3 + 4 * 5  "# => 35"`

!SLIDE bullets

# Cascade uses semi\-colons

* `# ruby`
* `a = 1; b = 2`

* `"# smalltalk"`
* `game := Game new board: newBoard; ui: newUi; playerX: newPlayerX; playerO: newPlayerO.`
* use `.` to terminate statements

!SLIDE small

# Booleans receive messages

        (1 + 1 = 2)
          ifTrue: [Transcript show: 'AWESOME']
          ifFalse: [Transcript show: 'NOT SO AWESOME'].

!SLIDE small

# Comparison syntax

        =  "# equality comparison"
        ==  "# identity comparison"

!SLIDE small

# Blocks

      block := [Transcript show: 'I''m a block!'].
      block value.  "# => I'm a block!"

### Common messages include: `collect:`, `select:`, `reject:`, `detect`, `inject:into:`

!SLIDE smaller

# Class Example

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

!SLIDE small

        | name age |  "# declares variables"

## Type of variable depends where variables are declared 

!SLIDE smbullets

## To create a Person object

* `|billy|`
* `billy := Person name: 'Charley' age: 12  "# => returns Charley (12)"`

!SLIDE smbullets

# Debugging

* respondsTo
* inspect
* explore
