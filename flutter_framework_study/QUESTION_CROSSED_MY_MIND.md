# Question Crossed My Mind
- [Good or Bad: Declaring main method async in Dart / Flutter](https://stackoverflow.com/questions/56129121/good-or-bad-declaring-main-method-async-in-dart-flutter)

## Does dart subclass can inherit named constructor from superclass?
- Ans: No. Remember that constructors are not inherited, which means that a superclass's named constructor is not inherited by a subclass. If you want a subclass to be created with a named constructor defined in the superclass, you must implement that constructor in the subclass.
for more detail read [Constructor](https://dart.dev/language/constructors#:~:text=Named%20constructors,-Use%20a%20named&text=Remember%20that%20constructors%20are%20not,that%20constructor%20in%20the%20subclass.)