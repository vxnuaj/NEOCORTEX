A static method is a method that belongs directly to a [[class]], not the instances created by a user.

To use a static method, you don't need to create an instance of a class nor will it ever have access to the variables defined by an instance of a class.

They're essentially regular functions that can be called through a class, often used as utility functions that don't depend on the state of a class.

For example:

```
class MyClass: 
def __init__(self, name): 
	self.name = name 
	
@staticmethod 
def static_method(): 
	print("This is a static method") 
	
def non_static_method(self): 
	print(f"This is a non-static method, my name is {self.name}") 
	
# Create an instance of the class 
obj = MyClass("John") 

# Call the static method 
MyClass.static_method() 

# OUTPUT: This is a static method 

# Call the non-static method 
obj.non_static_method() 

# Output: This is a non-static method, my name is John

```

