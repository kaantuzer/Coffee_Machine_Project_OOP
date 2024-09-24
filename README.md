Coffee Machine Project
This project simulates the operation of a coffee vending machine using object-oriented programming (OOP) principles in Python. The program allows a user to interact with a coffee machine by selecting drinks, checking resources, processing payments, and receiving coffee if the transaction is successful.

Features
Menu System: The machine provides multiple drink options (e.g., Latte, Espresso, Cappuccino) and allows users to select a drink.
Resource Management: The machine tracks its internal resources such as water, milk, and coffee and reports when ingredients are insufficient.
Money Handling: Users pay for their drinks by inserting coins. The machine handles different coin types, calculates the total, checks if the payment is sufficient, provides change if necessary, and updates the machine's profit.
Reports: The machine can generate reports showing its current resource levels and total profit.
Classes
1. MenuItem
Represents each drink item on the menu.

Attributes:
name: The name of the drink (e.g., "Latte", "Espresso").
ingredients: A dictionary that tracks the required amount of water, milk, and coffee for the drink.
cost: The price of the drink.
2. Menu
Manages the coffee machine’s menu, which includes available drinks.

Methods:
get_items(): Returns a string of all available drink names.
find_drink(order_name): Searches the menu for a drink by name and returns the corresponding MenuItem object, or notifies the user if the drink is not available.
3. CoffeeMaker
Manages the machine's resources and processes the actual preparation of drinks.

Attributes:
Tracks the current levels of water, milk, and coffee.
Methods:
report(): Prints the current levels of water, milk, and coffee.
is_resource_sufficient(drink): Checks if the machine has enough resources to make the selected drink.
make_coffee(drink): Deducts the required resources from the machine and "makes" the drink.
4. MoneyMachine
Handles payment processing and profit tracking.

Attributes:
profit: The total profit made by the machine.
money_received: The amount of money received from the user.
Methods:
report(): Prints the total profit earned.
process_coins(): Prompts the user to insert coins and calculates the total amount of money received.
make_payment(cost): Compares the amount of money received to the drink cost, returns change if necessary, and determines if the payment was successful.
Program Flow
The program starts by turning the coffee machine on (is_on=True) and enters a loop.
The user is prompted to select a drink from the menu, view a report, or turn off the machine.
If a drink is selected, the machine:
Checks if there are enough resources to make the drink.
Prompts the user to insert coins for payment.
Checks if the payment is sufficient and provides change if necessary.
Deducts the required resources and "serves" the drink.
The user can also request a report to see the current resource levels and total profit.
The machine will remain on until the user inputs "off," at which point it will close.
