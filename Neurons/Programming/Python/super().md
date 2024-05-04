`super()` allows us to access the methods of a parent class and call them within a given class.

Here's some sample usage

```
class Square:
	def __init__(self, height, width):
		self.height = height
		self.width = width
		self.area = None

	def s_area(self):
		self.area = self.height * self.width
		return self.area

class Rectangle(Square):
	def __init__(self, height, width):
		super().__init__(height, width)
		self.area = None
	
	def r_area(self):
		super().s_area() # you don't need to run the param, self
		return self.area
```


If we run:

```
if __name__ == "__main__":
	rec = Rectangle(2, 3)
	print(rec.r_area())
```

we'd get `6` as the output. This works because we initialized the methods and attributes of the class `Square` within the class `Rectangle` by setting the class argument of `Rectangle` to `Square` and calling it's `__init__()` method with `super()`. 

This method is typically used to simplify and reduce the lines of code by reducing the total lines of code