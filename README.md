# CS180-Project-5
### How to compile and run the program. 
1. Clone code into a text editor or IDE running Java 20.
2. Compile and run the program.
3. Follow the given prompts in the terminal and navigate the program with keyboard inputs.
4. Select the "Quit" option in the "WELCOME TO MARKETPLACE" page to save data for rerunning the program. 

### Aarav Gupta - Submitted report to Brightspace.
### Aarav Gupta - Submitted Vocareum workspace.

### MarketDriver.java
This class is where the program runs from and operates the control flow of the marketplace. The primary purpose of the MarketDriver class is likely to act as the driver or entry point for the application. It may handle user interface interactions, process user inputs, and coordinate communication with the backend logic.

This class works directly with MarketPlace.java. The MarketDriver class may handle user inputs, possibly through graphical user interfaces (GUIs) using Swing components. The interactions include creating accounts, logging in, and performing various actions within the marketplace.
MarketDriver allows for account management, such as creating a new account, logging in, changing usernames or passwords, and deleting accounts. It also includes the ability to add new stores, add products to stores, change product details, and remove products.
MarketDriver is important as it controls the overall navigation and flow of the application. 

### MarketPlace.java
This class works in tandem with MarketDriver.java. Originally all of the control flow of the program was in one class. However, to improve readability large chunks of code were moved to methods in this class. Essentially MarketPlace.java and MarketDriver.java work like a single class. For the functionality, relation to other classes, and testing, view the description of MarketDriver.java

### DataManager.java
This class stores all the user and market information in a text file so that data is preserved if you select quit program. DataManager methods are called from MarketPlace.java and use the hash maps storing all customers and users. All of the variables within each customer and user object are written to data.txt. This class also takes data.txt and parses through all the information to put all the customer and user objects back into the hash maps with their data saved.

This class' functionality is tested by running the program as intended: selling and buying objects, quitting the program, and seeing if the user login information, store stock, customer carts, and purchases have been saved if you run it again.

### Product.java
Product objects and the most basic object in this program store the product's seller, store, name, description, quantity, and price. The rest of this class is used to get and set these variables.

All other classes use and manipulate product objects. Store.java creates these objects which can be shown to customers to buy. Store.java also stores a list of purchased products. Customers can buy products that decrease their quantity.

Product.java itself does not need testing as it simply stores data.

### Store.java
This class is instantiated by a seller and stores an ArrayList of products, purchased products. Most methods within this class manipulate these ArrayLists. Similar to Product.java, this class stores data and logic concerning when that data is manipulated is called in MarketDriver.java and MarketPlace.java. 

Store.java itself does not need testing as it mostly stores and accesses data. Other methods such as editProduct and calculateOverallSales are simple and manually tested. 

### User.java
This class is a parent class of Seller and Customer. It is simple and has variables for username, password, and user which can be seller or customer. This class is made so that sellers and customers who extend it also have these variables.

The user object is operated on in MarketDriver.java and MarketPlace.java to log in with the right credentials and carry out the operations of a user.

This class does not need testing as it just ensures that sellers and customers have the necessary attributes.

### Seller.java
The seller class stores and manages an ArrayList of stores. This class stores data, and logic concerning when that data is manipulated is called in in MarketDriver.java and MarketPlace.java. 

Seller.java itself does not need testing as it mostly stores and accesses data.

### Customer.java
The customer class stores and manages an ArrayList of purchased items and the cart. This class stores data, and logic concerning when that data is manipulated is called in in MarketDriver.java and MarketPlace.java. 

Seller.java itself does not need testing as it mostly stores and accesses data.




