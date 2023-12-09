≤≤# CS180-Project-5
### How to compile and run the program. 
1. Clone code into a text editor or IDE running Java 20.
2. Compile and run the program.
3. Follow the given prompts in the terminal and navigate the program with keyboard inputs.
4. Select the "Quit" option in the "WELCOME TO MARKETPLACE" page to save data for rerunning the program. 

### Aarav Gupta - Submitted report to Brightspace.
### Aarav Gupta - Submitted Vocareum workspace.

### MarketDriver.java
This class is where the program runs from and operates the control flow of the marketplace. MarketDriver acts as the main entry point and user interface for the application. 

This class works in tandem with MarketPlace.java. The MarketDriver class may handle user inputs, possibly through graphical user interfaces (GUIs) using Swing components. The interactions include creating accounts, logging in, and performing various actions within the marketplace.
MarketDriver allows for account management, such as creating a new account, logging in, changing usernames or passwords, and deleting accounts. It also includes the ability to add new stores, add products to stores, change product details, and remove products.
MarketDriver is essential as it controls the overall navigation and flow of the application. 

### MarketPlace.java
This class works in tandem with MarketDriver.java. The MarketPlace class is the backend component that encapsulates the logic for managing the marketplace operations. It handles communication with the data store, validates user inputs, and executes various actions requested by MarketDriver or other parts of the application. Essentially MarketPlace.java and MarketDriver.java work like a single class.

### Product.java
This class represents a product in the system and includes information such as the seller, store, name, description, quantity, and price of the product.

It also interacts with other classes, maintaining reference to the Seller and Store classes, establishing relationships between products, sellers, and stores. This class is a fundamental building block for managing and representing items.

### Store.java
This class represents a store managed by a seller. It contains an ArrayList of products and additional lists to keep track of sales-related information. 

Store.java itself does not need testing as it mostly stores and accesses data.

### User.java
This class is a parent class of Seller and Customer. The class stores basic information about a user, including their username, password, and user type.

Testing is not needed for this class as it only ensures that sellers and customers have the necessary attributes.

### Seller.java
The seller class stores and manages an ArrayList of stores. The primary responsibility of a Seller is to manage one or more stores. The class includes an ArrayList named storeList that keeps track of the stores associated with a seller.

No testing needed for Seller.java

### Customer.java
This class represents a customer in the system and extends the User class. It includes features related to managing a customer's cart, purchased items, and the process of buying items. 

It includes an ArrayList 'cart' that represents the items currently in the customer's shopping cart as well as the purchasedList ArrayList that represents the items that the customer has already purchased.

### Pair.java
The Pair class is a generic class that can hold a pair of two objects, denoted as first and second.

This class can be used in various scenarios where a pair of objects needs to be stored together, providing a clean and generic way to do so.

### Server.java
This class is the main server component that handles communication with clients. 

The server maintains two HashMap objects: sellerMap and customerMap. These maps are used to store information about sellers and customers. The serialize method is used to serialize the sellerMap and customerMap objects and save them to files. The deserialize method reads the serialized objects from files and returns an array containing the deserialized sellerMap and customerMap.

### ServerThread.java
This class represents a thread that handles communication with a specific client. It interprets commands received from the client, processes them, and interacts with the server's data structures (sellerMap and customerMap).

It maintains ObjectOutputStream and ObjectInputStream streams for communication with the client via the Socket connection. 
The class handles various user commands, such as creating seller/customer accounts, setting the active user, setting the active product, and retrieving information about users, stores, and products. It interacts with the server's data structures (sellerMap and customerMap) to retrieve information as well as also performimg serialization of purchased products, export of products, and purchase history.

### ServerThread.java
This class is a generic class that represents a triple. It has three generic type parameters A, B, and C, allowing it to store three different types of values. 


