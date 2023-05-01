# Python_OOP
Object Oriented Programming in Python Programming Language

These questions are from my laboratory lessons. I tried to solve them and wanted to share with you.


#Question

-> Write a python class that represents a person.

- The class should have the following attributes: name, age, country, height, weight.
The class should have the following methods: set_name, set_age, set_country, set_height, set_weight.
The class should have the following methods: get_name, get_age, get_country, get_height, get_weight.

- The class should have the following magic methods: \_\_str\_\_<br>
The \_\_str\_\_ method should return a string contains the name, age, country, height, weight of the person.

- The get_name method should return the name of the person.
The get_age method should return the age of the person.
The get_country method should return the country of the person.
The get_height method should return the height of the person.
The get_weight method should return the weight of the person.

- The set_name method should set the name of the person.
The set_age method should set the age of the person.
The set_country method should set the country of the person.
The set_height method should set the height of the person.
The set_weight method should set the weight of the person.

-> Write a python class that represents a fireman which inherits from the Person class.

- The class should have the following attributes: name, age, country, height, weight, fireman_id, salary.
The class should have the following methods: set_fireman_id, set_salary.
The class should have the following methods: get_fireman_id, get_salary.

- The class should have the following magic methods: \_\_str\_\_
The \_\_str\_\_ method should return a string contains the name, age, country, height, weight, fireman_id, salary of the fireman.




#Answer

class Person:
    def __init__(self, name, age, country, height, weight):
        self.name = name
        self.age = age 
        self.country = country
        self.height = height
        self.weight = weight
        
    def set_name(self, name):
        self.name = name
    
    def set_age(self, age):
        self.age = age
    
    def set_country(self, country):
        self.country = country
    
    def set_height(self, height):
        self.height = height
        
    def set_weight(self, weight):
        self.weight = weight
    
    def get_name(self):
        return self.name 
    
    def get_age(self):
        return self.age
    
    def get_country(self):
        return self.country
    
    def get_height(self):
        return self.height
    
    def get_weight(self):
        return self.weight
    
    
    def __str__(self):
        return f'Name: {self.name}, Age: {self.age}, Country: {self.country}, Height: {self.height}, Weight: {self.weight}'
    
    
class Fireman(Person):
    
    def __init__(self, name, age, country, height, weight, fireman_id, salary):
        super().__init__(name, age, country, height, weight)
        self.fireman_id = fireman_id
        self.salary = salary
        
    def set_fireman_id(self, fireman_id):
        self.fireman_id = fireman_id
    
    def set_salary(self, salary):
        self.salary = salary
        
    def get_fireman_id(self):
        return self.fireman_id
    
    def get_salary(self):
        return self.salary
    
    def __str__(self):
        return f'Name: {self.name}, Age: {self.age}, Country: {self.country}, Height: {self.height}, Weight: {self.weight}, Fireman_ID: {self.fireman_id}, Salary: {self.salary}'

    
# Let us create a Person object 
    
person1 = Person('Mehmet Şahiner', 20, 'TR', 182, 65)
    
# Test time for Person
    
person1.set_name('Muhittin Ali Şahiner')   #My dad's and brother's names
print(person1.get_name())
print(person1.get_age())
print(person1.get_country())
print(person1.get_height())
print(person1.get_weight())
print(person1)

# Let us create a Fireman object

fireman1 = Fireman('Nisa Şahiner', 25, 'TR', 170, 50, 'ATEŞ321', 240000) #My sister's name

# Test time for Fireman

print(fireman1.set_name('İnci Şahiner')) #My mom' name
print(fireman1.get_name())
print(fireman1.get_age())
print(fireman1.get_country())
print(fireman1.get_height())
print(fireman1.get_weight())
fireman1.set_fireman_id('ATEŞ123')
fireman1.set_salary(250000)
print(fireman1.get_fireman_id())
print(fireman1.get_salary())
print(fireman1)



    
    

#Output

Muhittin Ali Şahiner
20
TR
182
65
Name: Muhittin Ali Şahiner, Age: 20, Country: TR, Height: 182, Weight: 65
None
İnci Şahiner
25
TR
170
50
ATEŞ123
250000
Name: İnci Şahiner, Age: 25, Country: TR, Height: 170, Weight: 50, Fireman_ID: ATEŞ123, Salary: 250000
