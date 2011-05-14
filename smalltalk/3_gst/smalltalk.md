!SLIDE

# What is GNU Smalltalk?

!SLIDE bullets incremental

## not a real Smalltalk implementation
* ...says the Smalltalk purist out in left field

!SLIDE smbullets incremental

### Nice transition, coming from another programming language

* if not coming from Ruby, great way to learn about message passing and OOP without being hindered by the Smalltalk environment

!SLIDE bullets incremental

### GNU Smalltalk website definition
## "The Smalltalk for those who can type"

* strips the Smalltalk environment away from you
* allows you to write to files
* with an editor/IDE of your choice
* with an SCM of your choice
* with great power, comes great responsibility

!SLIDE smbullets incremental

## Wikipedia definition

* dynamic, reflective, object-oriented programming language
* implements ANSI Smalltalk which is a descendant of Smalltalk-80
* supports message passing (inspired by Simula)
* everything is an object
* base classes are written entirely in Smalltalk (like Ruby)
* licensed under GNU LGPL

!SLIDE smbullets incremental

## What else?

* uses pre-emptive green threads
* VM is tucked away (similar to Java VM)
* but you could save/restore images like traditional Smalltalk implementations

!SLIDE

## In the REPL...

### `st> ObjectMemory snapshot: 'image.im'`

## In the console...

### `> gst -I image.im`

!SLIDE bullets incremental

### Somewhat recently, GNU Smalltalk started moving towards a traditional Smalltalk feel

* gst-blox - GUI building block tool kit
* gst-browser - class browser
* [VisualGST](http://visualgst.bioskop.fr/) - an IDE for GNU Smalltalk

!SLIDE bullets

# Only Five Reserved Words
### (they are really pseudo\-variables)

* `self`
* `super`
* `true`
* `false`
* `nil`
