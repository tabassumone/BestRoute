# BestRoute
Find the best route

Delivery Optimization System

Overview:
The Delivery Optimization System is a Java application designed to help delivery executives optimize their delivery routes for a batch of orders. It calculates the optimal delivery path considering the locations of consumers and restaurants, as well as the preparation times at each restaurant. The system exposes a REST API endpoint to receive input data and returns the optimal delivery path.

Features:
- REST API Endpoint: Provides an endpoint /orders/optimize-delivery to receive input data and return the optimal delivery path.
- Haversine Formula: Calculates the distance between two geo-locations using the Haversine formula.
- Optimization Logic: Implements a greedy approach to find the optimal delivery path by selecting the nearest restaurant for each order.
- Modular and Encapsulated Code: Utilizes object-oriented principles to create modular and encapsulated code.
- Error Handling: Includes basic error handling to handle exceptions gracefully.
- Production-ready: Follows best practices for production-ready Java code.


Usage:
To use the Delivery Optimization System, follow these steps:

- Input Data: Prepare input data including Aman's location, consumer locations, restaurant locations, and preparation times.
- Send HTTP POST Request: Send an HTTP POST request to the /orders/optimize-delivery endpoint with the input data in JSON format.


Example payload:
json

{
    "amanLocation": {"latitude": 12.9345, "longitude": 77.6100},
    "orders": [
        {"consumer": {"latitude": 12.9300, "longitude": 77.6200}, "restaurant": {"latitude": 12.9320, "longitude": 77.6150}, "prepTime": 15},
        {"consumer": {"latitude": 12.9400, "longitude": 77.6300}, "restaurant": {"latitude": 12.9420, "longitude": 77.6250}, "prepTime": 20}
    ]
}

Receive Response: Receive the optimal delivery path as a response from the system.

Assumptions:
- Coordinates are provided as latitude and longitude values.
- Preparation times for each restaurant are provided.
- Aman's current location is provided.
- The average speed of Aman is assumed to be 20 km/hr.

Running the Application:
- Build the project using Maven: mvn clean install.
- Run the Spring Boot application: java -jar delivery-optimizer.jar.

Extensibility:
- The Delivery Optimization System can be extended to handle more restaurants and delivery executives by adding additional locations and orders. Simply provide the input data accordingly, and the system will optimize the delivery path accordingly.

Testing:
- Unit tests can be added to ensure the correctness of individual components.
- Integration tests can be performed to validate the behavior of the system as a whole.


Contributors:
- Tabassum Ansari
- tabassumone@gmail.com
