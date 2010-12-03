!SLIDE smbullets incremental

# What is Smalltalk?

* dynamic, reflective, OOP
* supports message passing (inspired by Simula)

!SLIDE bullets incremental

# Three Types of Messages
### In order of precedence

* Unary
* Binary
* Keyword

!SLIDE bullets incremental

# Unary

* messages without arguments
* `'Hello World!' size.  "# => 12"`

!SLIDE smbullets

# Common Unary Messages

* subclass
* class
* new
* do
* ifTrue/ifFalse
* whileTrue/whileFalse
* isNil

!SLIDE bullets incremental small

# Binary

* messages with arguments (non\-alphabetic message)
* `1+2  "# => 3"`

!SLIDE smbullets incremental

# Keyword

* messages with one or more arguments
* `array at: 1 put: 'Hello!'.  "# => array := #('Hello!')"`
* selector is `at:put:` for the message

!SLIDE bullets

# Only Five Reserved Words
### (they are really pseudo\-variables)

* `self`
* `super`
* `true`
* `false`
* `nil`
