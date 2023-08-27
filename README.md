Пример использования абстрактного класса:

from abc import ABC, abstractmethod

class Shape(ABC):
    def __init__(self, color):
        self.color = color
    
    @abstractmethod
    def area(self):
        pass
    
    @abstractmethod
    def perimeter(self):
        pass
    
class Rectangle(Shape):
    def __init__(self, color, width, length):
        super().__init__(color)
        self.width = width
        self.length = length
    
    def area(self):
        return self.width * self.length
    
    def perimeter(self):
        return 2 * (self.width + self.length)
    
class Circle(Shape):
    def __init__(self, color, radius):
        super().__init__(color)
        self.radius = radius
    
    def area(self):
        return 3.14 * self.radius * self.radius
    
    def perimeter(self):
        return 2 * 3.14 * self.radius
    
rect = Rectangle("red", 5, 10)
print(rect.area()) # Output: 50
print(rect.perimeter()) # Output: 30

circle = Circle("blue", 2)
print(circle.area()) # Output: 12.56
print(circle.perimeter()) # Output: 12.56

Пример множественного наследования в Python:

class Animal:
    def __init__(self, name):
        self.name = name
    
    def eat(self):
        print(f"{self.name} is eating")
    
    def sleep(self):
        print(f"{self.name} is sleeping")
    
class Dog(Animal):
    def bark(self):
        print(f"{self.name} is barking")
    
class Bird(Animal):
    def fly(self):
        print(f"{self.name} is flying")

class DogBird(Dog, Bird):
    pass

dog_bird = DogBird("Buddy")
dog_bird.eat() # Output: Buddy is eating
dog_bird.sleep() # Output: Buddy is sleeping
dog_bird.bark() # Output: Buddy is barking
dog_bird.fly() # Output: Buddy is flying



