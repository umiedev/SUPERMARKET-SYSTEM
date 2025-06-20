# SUPERMARKET-SYSTEM
The C++ code provided implements a basic console-based Supermarket Management System. It allows for two primary types of users: Administrators and Buyers. The system manages product information, including product code, name, price, and discount, and stores this data in a text file named "database.txt"
# Supermarket Management System (C++)

## Project Description
This is a console-based Supermarket Management System developed in C++. It provides a fundamental framework for managing product inventory and handling customer purchases, catering to both administrative and buyer roles within a supermarket environment.

## Features

### Administrator Module
* **Login Authentication**: Secure access for administrators using predefined credentials.
* **Product Addition**: Add new products to the supermarket's inventory with unique product codes, names, prices, and discount percentages.
* **Product Modification**: Update existing product details, including product code, name, price, and discount.
* **Product Removal**: Delete products from the inventory.
* **Product Listing**: View a comprehensive list of all products currently available in the supermarket.

### Buyer Module
* **Product Listing**: Buyers can view all available products with their codes, names, and prices.
* **Product Purchase**: Select multiple products by code and specify quantities to build an order.
* **Duplicate Product Check**: Basic validation to prevent adding the same product multiple times in a single transaction during order creation.
* **Receipt Generation**: Automatically calculates the total bill, including discounts, and displays a detailed receipt for the purchase.

## How to Compile and Run

### Prerequisites
* A C++ compiler (e.g., g++).

### Compilation
1.  Save the provided C++ code as `miniproject.cpp`.
2.  Open a terminal or command prompt.
3.  Navigate to the directory where you saved `miniproject.cpp`.
4.  Compile the code using your C++ compiler (e.g., g++):
    ```bash
    g++ miniproject.cpp -o supermarket
    ```
    (Replace `supermarket` with your desired executable name.)

### Running the Application
1.  After successful compilation, run the executable:
    ```bash
    ./supermarket
    ```
    (On Windows, you might just type `supermarket.exe` or `supermarket`.)

## Usage

### Main Menu
Upon launching, the system will present a main menu:

To create a `README.md` file for your `miniproject.cpp`, we'll structure it to provide a clear overview for anyone looking at your code.

Here's the content for your `README.md` file:

```markdown
# Supermarket Management System (C++)

## Project Description
This is a console-based Supermarket Management System developed in C++. It provides a fundamental framework for managing product inventory and handling customer purchases, catering to both administrative and buyer roles within a supermarket environment.

## Features

### Administrator Module
* **Login Authentication**: Secure access for administrators using predefined credentials.
* **Product Addition**: Add new products to the supermarket's inventory with unique product codes, names, prices, and discount percentages.
* **Product Modification**: Update existing product details, including product code, name, price, and discount.
* **Product Removal**: Delete products from the inventory.
* **Product Listing**: View a comprehensive list of all products currently available in the supermarket.

### Buyer Module
* **Product Listing**: Buyers can view all available products with their codes, names, and prices.
* **Product Purchase**: Select multiple products by code and specify quantities to build an order.
* **Duplicate Product Check**: Basic validation to prevent adding the same product multiple times in a single transaction during order creation.
* **Receipt Generation**: Automatically calculates the total bill, including discounts, and displays a detailed receipt for the purchase.

## How to Compile and Run

### Prerequisites
* A C++ compiler (e.g., g++).

### Compilation
1.  Save the provided C++ code as `miniproject.cpp`.
2.  Open a terminal or command prompt.
3.  Navigate to the directory where you saved `miniproject.cpp`.
4.  Compile the code using your C++ compiler (e.g., g++):
    ```bash
    g++ miniproject.cpp -o supermarket
    ```
    (Replace `supermarket` with your desired executable name.)

### Running the Application
1.  After successful compilation, run the executable:
    ```bash
    ./supermarket
    ```
    (On Windows, you might just type `supermarket.exe` or `supermarket`.)

## Usage

### Main Menu
Upon launching, the system will present a main menu:
```
_________________________________________________________________________________
|                                                                                |
|                              Supermarket Main Menu                             |
|________________________________________________________________________________|

|                        (1) Administrator                     |
|                                                              |
|                        (2) Buyer                             |
|                                                              |
|                        (3) Exit                              |
```
* **Administrator (1)**: Requires login (Email: `admin@gmail.com`, Password: `admin@101`).
* **Buyer (2)**: Direct access to purchase products.
* **Exit (3)**: Terminates the application.

### Administrator Actions
* After logging in, administrators can choose to `Add`, `Modify`, or `Remove` products.
* The `list` function is automatically called to display current products before adding, editing, or removing.

### Buyer Actions
* Buyers can choose `Buy Product` to initiate an order.
* The system will first display all available products.
* Follow the prompts to enter product codes and quantities. You can add multiple products.
* The system will then generate your receipt.

## Project Structure
* `miniproject.cpp`: Contains the complete source code for the Supermarket Management System.
* `database.txt`: (Will be created automatically) A simple text file used to store product data persistently.

## Technical Details

* **Object-Oriented Programming (OOP)**: The system is primarily managed by a single `shopping` class, encapsulating all functionalities and data.
* **File Handling**: Utilizes `fstream` for reading from and writing product data to `database.txt`, ensuring persistence across sessions.
* **Basic Authentication**: A hardcoded email and password for administrator access.
* **`goto` statements**: Used for navigating back to menus within the application flow.
* **String and Numerical Processing**: Basic input/output operations for handling product details and calculating receipts.

## Limitations / Future Improvements
* **Error Handling**: More robust input validation (e.g., ensuring numeric input for prices/quantities, checking for negative values).
* **File Data Integrity**: Improve handling of file corruption or malformed data.
* **User Management**: Implement a more sophisticated user management system beyond a single hardcoded admin account.
* **Data Structures**: While functional, using `std::vector` or `std::map` in memory for product data and saving/loading the entire structure to/from file would improve performance for `receipt`, `edit`, and `rem` operations compared to repeated file reads/writes.
* **Search Functionality**: A dedicated search option for buyers.
* **Shopping Cart Persistence**: Currently, the buyer's cart is not saved if they exit the `receipt` function before completing.
* **Concurrency**: Not designed for multi-user access.
* **UI/UX**: Enhance the console interface for a more user-friendly experience.
```
