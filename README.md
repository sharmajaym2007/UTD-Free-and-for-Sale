# UTD-Free-and-for-Sale
Introduction
UTD Free and for Sale is intended to display advertisements for selling different products to students of UTD. Seller can the University itself or any student currently enrolled in UTD. It gives the users a single platform to view all the products segregated by categories.
The seller can post products for bidding by giving the base price or can sell a product at a firm price. For bidding process, the user with the highest bid will be able to buy the product. At the end of the bid, the buyer and the seller will get an email containing contact details of the other party. For products sold at firm price, the first user to click the buy button will be able to buy the product and will receive contact details of the seller.
Architecture:
 
Services:
•	Creating user account.
•	Posting advertisement for selling products.
•	Change Password.
•	Search for products.
Functionalities:
•	User can create account.
•	Users can update their password.
•	Users can list a product for selling.
•	Users can search for products by category.


Services
The API  that we provided
Creating user account.
 
With the register page a user can create their account. The client side validations are accomplished by JQuery and CSS elements. 
AJAX will send JSON data object using RESTful web service to server side class which will use the entity framework to return the requested response from the SQL database.
The user account information will be updated in the SQL database.

Search for products
 
This is the homepage where user is directed to when they search this website with the domain name. As you can see, either a user can search the product by keywords of product name and description in the text box on the top of side-bar on the left or directly by clicking on the images of category of products.The Nav bar on the top helps in navigation from Register page to Login page.Some links on the side-bar helps user understand the purpose of this website and how to make most of it.The user can go ahead and Login themselves in, which redirects them to a Login page where username and password credentials are asked.

The user credentials will be sent in JSON data object format to the server side controller, this in turn will use Entity framework which checks if this user credentials are present in database and according to that it will send response back to client. If registered he will be directed to Home page.

Posting advertisement for selling products

Information about the product is uploaded here which in turn is again sent by REST to server controller in JSON object by AJAX. Server controller will use Entity framework to save this information in product database.

Problems faced and their solution
1)	Image upload and display problem:
The issue with the upload image was regarding the type of data object used to store the image and send it to the database for storage.

Solution:
The BLOB data type of image was used where the image is converted to byte array and this data is stored in the database. This byte array is used in the display function where image is converted from byte array to image format as specified.

2)	MySQL support issue:
Initially we planned to use the MySQL with asp.net but there were limited functionalities associated with this.

Solution: 
We installed Microsoft SQL server 2012 for this purpose. Since these products are from the same manufacturer and it facilitates connecting and using database in Visual Studio in easier way.
