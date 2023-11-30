## Contributors

- Nishant Kumar ([@morya10](https://github.com/morya10)) (CDAC)
- Pawan Kumar Didwaniya ([@pawandidwaniya](https://github.com/pawandidwaniya)) (CDAC)
- Abhinav Kumar (CDAC)
- Prashant Anand (CDAC)
- Akshay Deshmukh (CDAC)

# Hungry Haven

This application provides restaurant owners and managers with a seamless and user-friendly web-based interface, empowering them to efficiently manage various aspects of their restaurant operations on the Hungry Haven platform. The intuitive design ensures that users can perform tasks effortlessly, resulting in an enhanced experience and increased participation of restaurants on Hungry Haven.


## Features

- **Menu Management:**
  - Restaurant managers/owners can easily add, update, or remove items from the menu.
  - Set item availability, prices, and manage the menu effortlessly.

- **Order Placement:**
  - Customers can browse the menu, add items to their cart, and place orders seamlessly.
  - Payment options available for customers, including card payments.

- **Delivery Services:**
  - Efficient delivery personnel management for timely order fulfillment.
  - Delivery personnel can set their availability for assignment by restaurant managers.

- **Order Tracking:**
  - Real-time tracking of the status of each order.
  - Delivery personnel can update the status of orders, keeping everyone informed.
## Screenshots

![Screenshot (64)](https://github.com/morya10/Hungry-Haven/assets/133471735/6a3601e5-5e34-47d3-b832-ed5bbccf8ea1)
![Screenshot (65)](https://github.com/morya10/Hungry-Haven/assets/133471735/3ae18886-0d6f-4780-a241-7ac96254a20a)
![Screenshot (66)](https://github.com/morya10/Hungry-Haven/assets/133471735/f6100bc4-e631-4268-84a5-c4334b8c63a7)
![Screenshot (67)](https://github.com/morya10/Hungry-Haven/assets/133471735/d50f709c-7365-4238-be61-acf8c0a8c87b)
![Screenshot (68)](https://github.com/morya10/Hungry-Haven/assets/133471735/0a100242-d1a8-40ea-a49e-d87ddec069b4)
![Screenshot (69)](https://github.com/morya10/Hungry-Haven/assets/133471735/e060c103-2950-4fa1-8e8b-495b36e66192)
![Screenshot (70)](https://github.com/morya10/Hungry-Haven/assets/133471735/086cd80d-d86f-4425-a4ef-4f29b8c003e2)
![img30](https://github.com/morya10/Hungry-Haven/assets/133471735/0af57892-0040-492f-b38d-68597268f673)
![img33](https://github.com/morya10/Hungry-Haven/assets/133471735/78eb2d2c-d98a-42f0-ba05-a6ec3587b0e7)
![img34](https://github.com/morya10/Hungry-Haven/assets/133471735/a0427e59-4475-462c-bf31-3536df675166)
![img37](https://github.com/morya10/Hungry-Haven/assets/133471735/df72598a-d270-4bfe-b1c0-db10713bbc6c)
![img40](https://github.com/morya10/Hungry-Haven/assets/133471735/42ee14ff-3860-4a0e-bf8e-c0934ffdcd59)
![img41](https://github.com/morya10/Hungry-Haven/assets/133471735/eb573a0b-fa00-4446-8217-868391e9c490)
![img44](https://github.com/morya10/Hungry-Haven/assets/133471735/72c3ce0b-589d-4c74-bcc9-f316acdb58ed)
![img47](https://github.com/morya10/Hungry-Haven/assets/133471735/615637a3-42aa-42b4-a2cc-a10fa00976cb)



## Development Stack
### Front-End

**Templates (Views):**
- HTML5
- CSS
- React.js
- Material-UI

**Service Layer:**
- React

### Back-End

**Rest Controllers, Exchanges, Services, Repository Services, Entities:**
- Java
- Spring Boot

### Data Store

**Database:**
- MySQL

### Tools

- REST API
- JSON
- Postman
- Spring Tool Suite (IDE)
## This Version
Current version has these flows implemented:
The current version includes the following implemented features:

- **Menu Management:**
  - Addition, removal, and editing of menu items.
  - Easy management of item attributes.

- **Inventory Management:**
  - Checking the quantity of items available.
  - Updating the quantity of items available.

- **Order Processing:**
  - Accepting/Rejecting incoming orders based on item availability.

- **Order Status Updates:**
  - Implementation of order status updates:
    - PREPARING
    - PACKED
    - Out For Delivery (OFD)
## API Contracts
Following APIs are developed on top of the current Hungry Haven backend:

### Customer Controller

#### User Authentication

- **Sign Up:**
  - **Endpoint:** POST /api/v1/customers/signup
  - **Description:** Add a new customer to the database.
  - **Request Body:** CustomerSignUpDto

- **Sign In:**
  - **Endpoint:** POST /api/v1/customers/signin
  - **Description:** Authenticate a customer.
  - **Request Body:** Credentials

#### Restaurant and Food Items

- **Get All Restaurants:**
  - **Endpoint:** GET /api/v1/restaurants
  - **Description:** Retrieve a list of all restaurants.

- **Get Food Items by Restaurant ID:**
  - **Endpoint:** GET /api/v1/fooditems/restaurant/{id}
  - **Description:** Retrieve food items from a specific restaurant.

- **Get Cart Items:**
  - **Endpoint:** POST /api/v1/fooditems/cart
  - **Description:** Retrieve selected items in the user's cart.
  - **Request Body:** ListOfFoodItemIds

#### Order Management

- **Update Customer Address:**
  - **Endpoint:** PUT /api/v1/customers/{id}/address
  - **Description:** Update the address of a customer.
  - **Request Body:** CustomerDto

- **Place Order:**
  - **Endpoint:** POST /api/v1/orders/place
  - **Description:** Place a new order.
  - **Request Body:** PlaceOrderDto

- **Get All Orders by Customer ID:**
  - **Endpoint:** GET /api/v1/orders/customer/{id}
  - **Description:** Retrieve all orders placed by a specific customer.

### Delivery Person Controller

#### Delivery Person Authentication

- **Sign In:**
  - **Endpoint:** POST /api/v1/deliveryperson/signin
  - **Description:** Authenticate a delivery person.
  - **Request Body:** Credentials

#### Delivery Person Homepage

- **Get Delivery Person Homepage Details:**
  - **Endpoint:** GET /api/v1/deliverypersonhomepage/{id}
  - **Description:** Retrieve details for the delivery person's homepage.
  - **Path Variable:** id (Delivery Person ID)

#### Order Management

- **Set Status by Order:**
  - **Endpoint:** POST /api/v1/deliveryperson/{orderId}/{status}
  - **Description:** Set the status of an order by a delivery person.
  - **Path Variables:** orderId (Order ID), status (Order Status)

- **Get All Orders by Delivery Person ID:**
  - **Endpoint:** GET /api/v1/orders/deliveryperson/{id}
  - **Description:** Retrieve all orders assigned to a specific delivery person.
  - **Path Variable:** id (Delivery Person ID)

- **Get Arrived Orders:**
  - **Endpoint:** POST /api/v1/deliveryperson/arrivedorders/{deliverypersonId}
  - **Description:** Retrieve arrived orders assigned to a delivery person.
  - **Path Variable:** deliverypersonId (Delivery Person ID)

- **Get Orders by Status:**
  - **Endpoint:** GET /api/v1/deliveryperson/{deliverypersonId}/status/{status}
  - **Description:** Retrieve orders assigned to a delivery person based on status.
  - **Path Variables:** deliverypersonId (Delivery Person ID), status (Order Status)

#### Delivery Person Registration

- **Delivery Person Sign Up:**
  - **Endpoint:** POST /api/v1/deliveryperson/signup
  - **Description:** Register a new delivery person.
  - **Request Body:** DeliveryPersonSignUpDto

### Restaurant Manager Controller

#### Restaurant Manager Authentication

- **Sign In:**
  - **Endpoint:** POST /api/v1/restaurantmanager/signin
  - **Description:** Authenticate a restaurant manager.
  - **Request Body:** Credentials

#### Restaurant Manager Information

- **Get Restaurant Manager by ID:**
  - **Endpoint:** GET /api/v1/restaurantmanager/{id}
  - **Description:** Retrieve details of a restaurant manager by ID.
  - **Path Variable:** id (Restaurant Manager ID)

#### Delivery Person Management

- **Get Available Delivery Persons:**
  - **Endpoint:** GET /api/v1/restaurantmanager/availabledeliveryperson/{status}
  - **Description:** Retrieve available delivery persons.
  - **Path Variable:** status (Boolean indicating availability)

#### Order Management

- **Get Arrived Orders:**
  - **Endpoint:** POST /api/v1/restaurantmanager/arrivedorders/{restaurantId}
  - **Description:** Retrieve arrived orders for a specific restaurant.
  - **Path Variable:** restaurantId (Restaurant ID)

- **Get All Orders by Restaurant ID:**
  - **Endpoint:** POST /api/v1/restaurantmanager/allorders/{restaurantId}
  - **Description:** Retrieve all orders for a specific restaurant.
  - **Path Variable:** restaurantId (Restaurant ID)

#### Food Item Management

- **Add Food Item:**
  - **Endpoint:** POST /api/v1/restaurantmanager/addfooditem
  - **Description:** Add a new food item to the restaurant's menu.
  - **Request Body:** FoodItemHomePageDto

- **Get All Food Types:**
  - **Endpoint:** GET /api/v1/foodtypes
  - **Description:** Retrieve all available food types.

- **Get Food Item Details for Editing:**
  - **Endpoint:** GET /api/v1/foodTypes/edit/{foodItemId}
  - **Description:** Retrieve details of a food item for editing.
  - **Path Variable:** foodItemId (Food Item ID)

- **Update Food Item Details:**
  - **Endpoint:** POST /api/v1/foodTypes/edit/{foodItemId}
  - **Description:** Update details of a food item.
  - **Request Body:** FoodItemHomePageDto

#### Orders Assignment

- **Assign Delivery Person to Order:**
  - **Endpoint:** POST /api/v1/orders/assign/{orderId}/{deliveryPersonId}
  - **Description:** Assign a delivery person to an order.
  - **Path Variables:** orderId (Order ID), deliveryPersonId (Delivery Person ID)

#### Restaurant and Restaurant Manager Sign Up

- **Sign Up:**
  - **Endpoint:** POST /api/v1/restaurantmanager/signup
  - **Description:** Sign up a new restaurant and restaurant manager.
  - **Request Body:** RestManAndRestSignUpDto

## Development Guide
The project is organized into two main folders:

- `/backend`: Contains all the backend-related code.
- `/frontend`: Houses all the frontend-related code.
## Links
https://docs.google.com/document/d/1GREbZjQGaydK41JkfP6nijgZPAzglNYm/edit?usp=drive_link&ouid=100481243189702669506&rtpof=true&sd=true
