# The SOLID design principles

## Single Responsibility Principle / Seperations of Concerns
- A class should have one responsiblity. For example, if you have a journal class that has methods that create and stores entries you sould not add methods to the class that also do something completely different like storing that journal to a file.

-Generalized funtionality that may be used across multiple classes such as a method for write data to a file should be have their own class. Centralizing this functionality allows us to reuse and maintain our code in a simpler way.


## Open Closed Principle - open for extention, closed for modification
- When you add functionality to a class, you add by extention, not modification. This goes for existing classes that have been implemented 
and tested already to prevent side effects from modifying code. 

- Creating small filter and specification classes with methods is best practice. Do not modifiy classes that run perfectly fine as is and play a
part in your code. Add others to get the functionality that you want.

## LSP Liskov Substituion Principle
- interface -> base_class -> derived_class

- if an interface takes a base class, substiting in a derived class should not throw an exception. 

ex. interface     | def show_area(shape)
    base class    | class shape(height, width) -> has height/width setters
    derived class | class circle(shape) -> modifies height/width making them
                    turning them into a diameter radius
    result        | show_area(shape) -> shape.width * shape.height will not
                    return the area of the circle, throwing an exception. 

### Interface Segragation Principle
- Split interfaces into the smallest slices possible so you are able to build off of them using inheiritance. Building large interfaces will carry over methods to subclasses that do not need them but still can access. This can cause issues, do not create subclasses from classes that do not or cannot use the superclasses functionality. Break up and inhierit what you need.