# python5

class Superhero:
    """Represents a superhero with unique attributes and abilities."""

    def __init__(self, name, secret_identity, power, weakness, catchphrase):
        """Initializes a Superhero object.

        Args:
            name (str): The superhero's public name.
            secret_identity (str): The superhero's hidden identity.
            power (str): The superhero's primary superpower.
            weakness (str): The superhero's main vulnerability.
            catchphrase (str): The superhero's signature saying.
        """
        self.name = name
        self.secret_identity = secret_identity
        self.power = power
        self.weakness = weakness
        self.catchphrase = catchphrase
        self.battles_won = 0

    def reveal_identity(self):
        """Reveals the superhero's secret identity."""
        print(f"By day, I am the unassuming {self.secret_identity}...")

    def use_power(self):
        """Demonstrates the superhero using their power."""
        print(f"With incredible focus, {self.name} unleashes their mighty {self.power}!")

    def face_weakness(self):
        """Describes the superhero's reaction to their weakness."""
        print(f"Oh no! {self.weakness} is affecting {self.name}!")

    def say_catchphrase(self):
        """The superhero delivers their iconic catchphrase."""
        print(f'"{self.catchphrase}!" declares {self.name}.')

    def increase_wins(self):
        """Increments the number of battles won."""
        self.battles_won += 1
        print(f"{self.name}'s victory count rises to {self.battles_won}!")

class FlyingSuperhero(Superhero):
    """Represents a superhero who can fly, inheriting from Superhero."""

    def __init__(self, name, secret_identity, power, weakness, catchphrase, flight_speed):
        """Initializes a FlyingSuperhero object.

        Args:
            name (str): The superhero's public name.
            secret_identity (str): The superhero's hidden identity.
            power (str): The superhero's primary superpower.
            weakness (str): The superhero's main vulnerability.
            catchphrase (str): The superhero's signature saying.
            flight_speed (str): The superhero's speed in flight.
        """
        super().__init__(name, secret_identity, power, weakness, catchphrase)
        self.flight_speed = flight_speed

    def fly(self):
        """Demonstrates the flying superhero taking to the skies."""
        print(f"{self.name} soars through the air at {self.flight_speed}!")

# Creating instances of the classes
superman = Superhero("Superman", "Clark Kent", "Super Strength and Flight", "Kryptonite", "Truth, Justice, and the American Way!")
wonder_woman = Superhero("Wonder Woman", "Diana Prince", "Super Strength and Lasso of Truth", "Binding by a male", "For Justice!")
hawkman = FlyingSuperhero("Hawkman", "Carter Hall", "Flight and Nth Metal Weapons", "Cold", "Justice will prevail!")

# Interacting with the objects
superman.reveal_identity()
superman.use_power()
superman.increase_wins()
wonder_woman.say_catchphrase()
hawkman.fly()
hawkman.face_weakness()


2.POLYMORPHISM CHALLENGE

class Animal:
    """Base class for animals with a generic move action."""
    def move(self):
        print("This animal moves in a general way.")

class Car:
    """Represents a car with a specific move action."""
    def move(self):
        print("Driving ")

class Plane:
    """Represents a plane with a specific move action."""
    def move(self):
        print("Flying ")

class Snake(Animal):
    """Represents a snake with a specific move action."""
    def move(self):
        print("Slithering ")

class Fish(Animal):
    """Represents a fish with a specific move action."""
    def move(self):
        print("Swimming ")

# Creating a list of different objects
things_that_move = [Car(), Plane(), Snake(), Fish()]

# Demonstrating polymorphism
print("Demonstrating Polymorphism:")
for thing in things_that_move:
    thing.move()



