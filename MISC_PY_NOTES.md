# Misc python notes

### Attributes vs Properties
- Attributes are a data members of an object, Properties are
methods in an object that are accessed like attributes but
perform computaion. 

- public attributes are availalbe to the user to modify, it
is best that these be converted to private attributes and use
getters and setters to modifiy and access.

- private attributes are created by prepending __ to an attribute. they can only be accessed inside of the class.

### __str__
- this dunder returns the string representation of an object. 
ex. 
    def __str__(self):
        yield f"This is your name: {self.name}"
    
    print(exobj) -> "This is your name: exobject"


### interface (possibly refered to as a superclass) (general programming term)
- A junction point where classes are implemented to produce functionality in a program. An interface takes in a class and invokes methods from a the class. Classes that are used with the interface should all follow the Liskov substitution principle to prevent exceptions.

### getters (accessor) and setters (mutator) (general programming term)
- getters and setters are used to access and modify a class's an attribute in a class

- To implement them, you must make your attributes non-public, and then make getter and setter methods for all of the attributes.

