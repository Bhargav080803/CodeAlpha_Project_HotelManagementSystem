This Java code implements a simple Hotel Reservation System with functionality to manage rooms and reservations. Here's an explanation of the code:

1. Room Class:
   - Represents a room in the hotel.
   - Attributes:
     - `roomNumber`: The unique identifier for each room.
     - `isAvailable`: Indicates whether the room is available for reservation.
   - Constructors to initialize the room with a room number and availability status.
   - Accessor methods to get the room number and availability status.
   - Method `setAvailability` to update the availability status of the room.

2. Reservation Class:
   - Represents a reservation made by a guest.
   - Attributes:
     - `guestName`: Name of the guest making the reservation.
     - `roomNumber`: Room number reserved.
     - `numOfDays`: Number of days for the reservation.
   - Constructor to initialize a reservation with guest name, room number, and number of days.
   - Accessor methods to retrieve guest name, room number, and number of days.

3. Hotel Class:
   - Manages hotel operations such as initializing rooms, displaying available rooms, making reservations, etc.
   - Connects to a MySQL database to store room information and reservations.
   - Attributes:
     - `rooms`: List to store Room objects.
     - `reservations`: List to store Reservation objects.
   - Constructor `Hotel(int numRooms)`:
     - Initializes rooms by fetching data from the database or creating new rooms if necessary.
   - Method `displayAvailableRooms()`:
     - Displays available rooms by iterating through the list of rooms and checking their availability.
   - Method `saveReservationsToDatabase()`:
     - Saves reservations to the database.
   - Method `makeReservation(String guestName, int roomNumber, int numOfDays)`:
     - Attempts to make a reservation for a guest.
     - Checks if the requested room is available and updates its availability.
     - Creates a new Reservation object and adds it to the reservations list.
     - Calls `saveReservationsToDatabase()` to save the reservation details.
   - Method `findRoom(int roomNumber)`:
     - Finds a room by its room number.
   
4. HotelReservationSystem1 Class (Main Class):
   - Contains the main method to interact with users.
   - Displays a menu with options to display available rooms, make reservations, or exit the system.
   - Accepts user input and invokes corresponding methods of the Hotel class based on the selected option.

Overall, this code provides a basic framework for managing hotel reservations through a console-based interface while utilizing a MySQL database for data storage.
