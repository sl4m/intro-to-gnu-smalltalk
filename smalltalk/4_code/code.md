!SLIDE bullets

# Comments

* `# ruby`
* `#`

* `"smalltalk"`
* `""`

!SLIDE bullets

# Characters are not Strings

* `# ruby`
* `'a'.class  # => String`

* `"smalltalk"`
* `'a' class  "# => String"`
* `$a class  "# => Character"`

!SLIDE bullets

# Quote Escaping in Strings

* `# ruby`
* `'Hello "world"'`
* `"Hello 'world'"`
* `"Hello \"world\""`

* `"smalltalk"`
* `'Hello ''world'''`

!SLIDE bullets

# Symbols

* `# ruby`
* `:foo_bar`

* `"smalltalk"`
* `#fooBar`

!SLIDE bullets

# Arrays

* `# ruby`
* `[0, 1, 2]`

* `"smalltalk"`
* `#(0 1 2)`
* `{0 . 1 . 2}`

!SLIDE bullets

## Meaning of Binary Messages are not "hard\-wired"
## They are all treated the same

* `# ruby`
* `3 + 4 * 5  # => 23`

* `"smalltalk"`
* `3 + 4 * 5  "# => 35"`

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

!SLIDE smbullets

## To create a Person object

* `|billy|`
* `billy := Person name: 'Charley' age: 12  "# => returns Charley (12)"`

!SLIDE small

# Recursion Example

        factorial
            "Answer the factorial of the receiver."

            self = 0 ifTrue: [^ 1].
            self > 0 ifTrue: [^ self * (self - 1) factorial].
            self error: 'Not valid for negative integers' 

