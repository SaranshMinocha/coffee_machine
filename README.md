Python OOP Beginner
☕ OOP Coffee Machine
A command-line coffee machine simulator built with object-oriented programming
Simulates a real coffee machine — tracks ingredients, handles payments, and brews drinks — using four decoupled classes. Each class owns exactly one responsibility.

Classes
Menu
Holds available drinks and finds a drink by name
MenuItem
Represents a single drink with ingredients and cost
CoffeeMaker
Tracks resources, checks sufficiency, makes the drink
MoneyMachine
Processes coin input, validates payment, tracks profit
Program flow
1
User is prompted to pick a drink from menu.get_items()
2
menu.find_drink(choice) returns the matching MenuItem object
3
coffee_maker.is_resource_sufficient(drink) checks water, milk, coffee levels
4
money_machine.make_payment(drink.cost) collects coins and validates total
5
If both pass → coffee_maker.make_coffee(drink) deducts resources and serves
Commands
espresso / latte / cappuccino
Order a drink
report
Print current resource & profit status
off
Shut down the machine
Run it
git clone https://github.com/SaranshMinocha/<repo-name> cd oop-coffee-machine python main.py
Project structure
oop-coffee-machine/ ├── main.py # Entry point, main loop ├── menu.py # Menu + MenuItem classes ├── coffee_maker.py # CoffeeMaker class └── money_machine.py # MoneyMachine class
