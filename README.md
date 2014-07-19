1. Implementation of each method in Calculator.java: 5%
   <br>  -> 25%
2. Test Cases:
<br>\- Add/ Subtract: 
	<br>&nbsp;&nbsp;&nbsp;&nbsp;Positive number, zero and negative number should be considered: 5% for Add/ 5% for Subtract
	<br>&nbsp;&nbsp;&nbsp;&nbsp;Max value should be considered: 5% for Add/ 5% for Subtract
    <br> -> 20%
<br>\- Multiply: 
	<br>&nbsp;&nbsp;&nbsp;&nbsp;Negative number multiply positive number: 5%
	<br>&nbsp;&nbsp;&nbsp;&nbsp;Any number multiply zero: 5%
	<br>&nbsp;&nbsp;&nbsp;&nbsp;Negative number multiply negative number or positive number multiply negative number: 5%
	<br> -> 15%
<br>\- Divide: 
	<br>&nbsp;&nbsp;&nbsp;&nbsp;Negative number divided by positive number: 5%
	<br>&nbsp;&nbsp;&nbsp;&nbsp;The result of the division has infinite decimals: 5%
	<br>&nbsp;&nbsp;&nbsp;&nbsp;Any number divided by zero: 5%
	<br> -> 15%
<br>\- Other good ideas in test cases: 5%
	-> 5%

3. 
<br>Correct folder structures and consistent package names: 10%
<br>Correct version of JUnit test cases: 5%
<br>Commit ID submission: 5%
<br>-> 20%



Coffee Cart Android Application

Android Version: 4.0(minimum required) - 4.4.2

Package: edu.gatech.cc.cs6300.online.coffeecart
- Activity classes are used to control the transaction flow. The associations are all implemented in these classes.

Package: edu.gatech.cc.cs6300.online.coffeecart.database
- All the classes related to database operations.

  Database Design:
  - 4 tables: Customer, Item, Transaction, TransactionItems
  - Customer: Contains all the customer info
  - Item: Contains all the item (including dessert and coffee) info
  - Transaction: Transactions have 3 types including purchases, refills and preorders. In this table, it contains the following columns: transaction id, customer id, transaction type, preorder date (if there is), total price and the transaction timestamp.
  - TransactionItems: Contains the transaction details - the item list and corresponding amounts.

Package: edu.gatech.cc.cs6300.online.coffeecart.entity
- The entities that is stored in the database. This includes all the classes in the class diagram.

Package: edu.gatech.cc.cs6300.online.coffeecart.utility
- Some utility operations like cardnumber validation.

Problems:

1. Whether customer should pay for preorder?
-> I assume all the preorder should be paid and the price is the total price of the ordered desserts.

2. Whether the money in purchase also includes the money spent on refills?
-> I assume purchase and refill are different transactions.

3. How should the customer check out? Right after order or just before leaving?
-> I assume the customer should pay when they are purchasing, asking for refills and preordering.

4. The database design doesn't use different tables to distinguish between dessert and coffee, and among purchase, refill and preorder. So whether the entities in the entity package should also be changed according to the tables? If so, PreOrder class, Purchase class, Dessert class and Coffee class are not necessary any more, this is not consistent with our original design. 

Usage: 

- Input a VIP Card Number and click "Submit", then you can manage the customer's info, purchase/refill/preorder items and view the transaction history.
<br>&nbsp;&nbsp;(1) Available VIP Card Numbers:
<br>&nbsp;&nbsp;&nbsp;&nbsp;-> 1234567890
<br>&nbsp;&nbsp;&nbsp;&nbsp;-> 1234567891
<br>&nbsp;&nbsp;&nbsp;&nbsp;-> 1234567892

<br>&nbsp;&nbsp;(2) Add New Customers and then "login" with the generated VIP Card Number. Please remember the number by viewing the customer's info (click "Details" button). Same with #2.

- Add a new customer by entering the necessary information. The system will direct to the customer's home page after it is created.

- See the PreOrders those are picked up today.

- See the Purchases/Refills today.



