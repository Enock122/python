Assignment 1: Design Your Own Class! 
# Base class
class Smartphone:
    def __init__(self, brand, model, price):
        self.brand = brand
        self.model = model
        self.price = price

    def call(self, number):
        print(f"{self.brand} {self.model} is calling {number}...")

    def specs(self):
        return f"Brand: {self.brand}, Model: {self.model}, Price: ${self.price}"

# Subclass inheriting from Smartphone
class GamingPhone(Smartphone):
    def __init__(self, brand, model, price, gpu, refresh_rate):
        super().__init__(brand, model, price)
        self.gpu = gpu
        self.refresh_rate = refresh_rate

    def gaming_mode(self):
        print(f"{self.brand} {self.model} is in Gaming Mode with {self.gpu} and {self.refresh_rate}Hz refresh rate!")

# Creating objects
phone1 = Smartphone("Apple", "iPhone 15", 1200)
gaming_phone = GamingPhone("Asus", "ROG Phone 7", 1400, "Adreno 730", 165)

# Calling methods
print(phone1.specs())
phone1.call("+123456789")

print(gaming_phone.specs())
gaming_phone.gaming_mode()

Activity 2: Polymorphism Challenge! 🎭
# Base class
class Vehicle:
    def move(self):
        pass

# Subclasses with different implementations of move()
class Car(Vehicle):
    def move(self):
        print("🚗 The car is driving on the road.")

class Plane(Vehicle):
    def move(self):
        print("✈️ The plane is flying in the sky.")

class Boat(Vehicle):
    def move(self):
        print("🚢 The boat is sailing on the water.")

# Creating objects and demonstrating polymorphism
vehicles = [Car(), Plane(), Boat()]

for vehicle in vehicles:
    vehicle.move()
