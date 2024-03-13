# Blue-sky-Booking-system
In summary, the airline ticket booking system is a crucial element of the modern travel business, changing the booking and purchase of airline tickets for a worldwide customer base. Through the use of cutting-edge technology and internet platforms, this system has greatly increased trip booking efficiency, accessibility, and convenience.

class User:

  def_init_(self, user_id, name, email):

    self.userld=user_id

    self.name = name

    self.email = email

class Flight:

          def_init_(self, flight_id, airline, departure, destination, departure_time,

available_seats):

     self.flightId = flight_id

     self.airline = airline

     self.departure = departure

     self.destination = destination

     self.departure Time = departure_time

     self.availableSeats = available_seats

class Booking:

  def_init_(self, booking_id, user, flight):

       self.bookingId = booking_id

       self.user=user

       self.flight = flight

       self.booking Time = datetime.now()

class Payment:

     def_init_(self, payment_id, booking, amount):

       self.paymentId = payment_id

       self.booking = booking

       self.amount = amount

       self.paymentTime = datetime.now()

class BookingEngine:

   def check_availability(self, flight):

     return flight.availableSeats > 0

  def book flight(self, user, flight):

    if self.check_availability(flight):

      booking_id = hash((user.userld, flight. flightld, datetime.now()))

      return Booking(booking_id, user, flight)

else:

      print("Sorry, the flight is fully booked.")

      return None
      
class PaymentSystem:

    def process_payment(self, booking, amount):

      payment_id = hash((booking.bookingld, datetime.now()))

      return Payment(payment_id, booking, amount)

User inputs:-

# Example usage:

user = User(1, "John Doe", "john.doe@example.com")

flight = Flight(101, "Airline X", "City A", "City B", datetime (2023, 1, 1), 50)

    booking_engine = BookingEngine()

    booking booking_engine.book_flight(user, flight)

if booking:

   payment_system = PaymentSystem()

   payment = payment_system.process_payment(booking, 500.0)

   print("Booking successful!")

   print(f"Booking ID: {booking.bookingld}")

   print(f"Payment ID: {payment.paymentId}")

   print(f"Amount Paid: (payment.amount}")

else:

print("Booking unsuccessful.")
