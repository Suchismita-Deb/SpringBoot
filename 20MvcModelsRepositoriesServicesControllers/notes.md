Separation of Concerns. 

The code should not be tightly coupled.
Models - Business Logic.
In Monolith also we can have MVC and in Microservices we have MVC.
MVc is like architecture. For writing backend logic we use Mvc. 

The View is handled by frontend part. We have API view handle by react and that connected to Backend.

Business logic has many things involved like Algorithms(Services), Entities(representation of teh table in the class, in place of REST if we are using GRPC then we use Protocol Buffers and it creates the classes), Data Interactions(query the table repository).

Controller handles the request. If any request comes and controller not aware of it so there should be some type of validation. When controller gets the request should first pass to the validators.


Say in ecommerce application after making the order it should send a message to the user, the SMTP is not written in the business layer and say the app uses third party messaging system then teh service layer should interact with another API Layer. There are different API layer to interact with third party system. Like the payment gateway.



We also have DTO that has teh data required in the contract. In razorpay it ask for teh user and payment mode and the id and all these are needed to send to the API layer handling the payment. These data are handled in the DTO.
DTO is also present in Controllers. When controllers is expecting an API to send a request body. The request body is going to be accepted as a class object. Spring will convert and we should have the classs written properly. 
DTO is used for the API contract object creation.

The repository layer is often referred as DAO. 
> Sometimes the Repository and the Entity are clubbed together and placed as Persistent Layer.

