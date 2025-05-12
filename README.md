# class ACTIVITY 1 (Custom Class with Inheritance and Encapsulation)
# Base class
class Vehicle:
    def __init__(self, brand, model, year):
        self.brand = brand          # Public attribute
        self._model = model         # Protected attribute
        self.__year = year          # Private attribute

    def get_year(self):
        return self.__year

    def display_info(self):
        print(f"{self.brand} {self._model}, Year: {self.__year}")

    def move(self):
        print("The vehicle is moving...")

# Subclass Car
class Car(Vehicle):
    def __init__(self, brand, model, year, fuel_type):
        super().__init__(brand, model, year)
        self.fuel_type = fuel_type

    def move(self):
        print(f"{self.brand} {self._model} is driving on the road! 🚗")

# Subclass Plane
class Plane(Vehicle):
    def __init__(self, brand, model, year, engine_type):
        super().__init__(brand, model, year)
        self.engine_type = engine_type

    def move(self):
        print(f"{self.brand} {self._model} is flying in the sky! ✈️")

# Subclass Boat
class Boat(Vehicle):
    def __init__(self, brand, model, year, boat_type):
        super().__init__(brand, model, year)
        self.boat_type = boat_type

    def move(self):
        print(f"{self.brand} {self._model} is sailing on the water! 🚢")

ACTIVITY 2 POLYMORPHYSIM IN ACTION
# Create instances of each class
car = Car("Toyota", "Camry", 2022, "Petrol")
plane = Plane("Boeing", "747", 2018, "Jet")
boat = Boat("Yamaha", "WaveRunner", 2020, "Jet Ski")

# Polymorphism: Call the same method on different objects
vehicles = [car, plane, boat]

for vehicle in vehicles:
    vehicle.move()

