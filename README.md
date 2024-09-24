# Hexaware_Assignment_TicketBookingSystem

This project, TicketBookingSystem, is a database designed to manage a ticket booking system for various events like movies, concerts, and plays. The database is built in MS SQL Server and consists of four key tables: Venue, Event, Customer, and Booking. The relationships between these tables allow for efficient management of event information, customer data, and booking transactions. Here's an overview of the structure and functionality:

Database Structure :

1 - Venue Table
Stores information about venues where events are held.

Attributes:
venue_id: Primary key for unique identification of venues.
venue_name: Name of the venue.
address: Location of the venue.

2 - Event Table
Holds data about various events available for booking, such as movies, concerts, or plays.

Attributes:
event_id: Primary key for event identification.
event_name: Name of the event.
event_date: The date of the event.
event_time: The time the event is scheduled to start.
venue_id: Foreign key referencing the Venue table.
total_seats: Total seats available for the event.
available_seats: Seats that are still available for booking.
ticket_price: Price of a single ticket for the event.
event_type: Type of the event (Movie, Concert, Play).
booking_id: Foreign key referencing the Booking table.

3 - Customer Table
Stores customer information who book tickets for events.

Attributes:
customer_id: Primary key for identifying customers.
customer_name: Name of the customer.
email: Customer's email address.
phone_number: Customer's phone number.
booking_id: Foreign key referencing the Booking table.

4 - Booking Table
Maintains records of bookings made by customers for different events.

Attributes:
booking_id: Primary key for booking transactions.
customer_id: Foreign key referencing the Customer table.
event_id: Foreign key referencing the Event table.
num_tickets: Number of tickets booked for the event.
total_cost: Total cost calculated based on the number of tickets booked.
booking_date: The date the booking was made.
