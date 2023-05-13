# OOPS_ASSIGNMENT

# Challenge 1 : Square Numbers and Return Their Sum

class Point:
    def __init__(self,x,y,z):
        self.x = x
        self.y = y
        self.z = z
    def sqSum(self):
        return self.x**2 + self.y**2 + self.z**2
point = Point(1,3,4)
print(point.sqSum())                                

# OUTPUT 
26





# Challenge 2 : Implement a Calculator Class

class Calculator:

    def __init__(self,x,y):
        self.x = x
        self.y = y
        
    def add(self):
        return self.x + self.y
    def subtract(self):
        return self.x - self.y
    def multiply(self):
        return self.x * self.y
    def divide(self):
        return self.x / self.y
x=int(input("Enter the num1:"))
y=int(input("Enter the num2"))
calculator = Calculator(x,y)
print("Addition :",calculator.add())      
print("Subtraction:" , calculator.subtract()) 
print("Multiplication:",calculator.multiply()) 
print("Division:",calculator.divide())

# OUTPUT
 Enter the num1:20 \n
 Enter the num210
 Addition : 30
 Subtraction: 10
 Multiplication: 200
 Division: 2.0





# Challenge 3 : Implement the Complete Student Class

class Student:
    def __init__(self):
        self.__name = ""
        self.__rollNumber = ""

    def setName(self, name):
        self.__name = name

    def getName(self):
        return self.__name

    def setRollNumber(self, rollNumber):
        self.__rollNumber = rollNumber

    def getRollNumber(self):
        return self.__rollNumber
student = Student()
student.setName("Harsh")
student.setRollNumber(200390)
print(student.getName())
print(student.getRollNumber()) 

# OUTPUT
Harsh
200390 




# Challenge 4: Implement a Banking Account

class Account:
    def __init__(self, title, balance):
        self.title = title
        self.balance = balance

class SavingsAccount(Account):
    def __init__(self, title, balance, interestRate):
        super().__init__(title, balance)
        self.interestRate = interestRate
savingsAccount1 = SavingsAccount("Ashish", 5000, 5)
print(savingsAccount1.title)         
print(savingsAccount1.balance)       
print(savingsAccount1.interestRate)  

# OUTPUT
Ashish
5000
5



# Challenge 5: Handling a Bank Account

class Account:
    def __init__(self, title=None, balance=0):
        self.title = title
        self.balance = balance
    
    def withdrawal(self, amount):
        self.balance -= amount

    def deposit(self, amount):
        self.balance += amount
        
    def getBalance(self):
        return self.balance

class SavingsAccount(Account):
    def __init__(self, title=None, balance=0, interestRate=0):
        super().__init__(title, balance)
        self.interestRate = interestRate
    
    def interestAmount(self):
        return (self.balance * self.interestRate)/100

#code to test - do not edit this

demo1 = SavingsAccount("Ashish", 2000, 5)
demo1.deposit(500)
print(demo1.getBalance())   
demo1.withdrawal(500)
print(demo1.getBalance())   
print(demo1.interestAmount())

# OUTPUT
2500
2000
100.0



