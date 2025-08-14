# Level 1 Final Project -- Movie Ticket Booking System

## Slide 1 -- Title

**Movie Ticket Booking System**\
Level 1 -- Final Project\
Topics Covered: Variables, Data Types, IO, Conditions, Loops, Arrays,
Strings, ArrayList, Methods, Basic Classes/Objects

------------------------------------------------------------------------

## Slide 2 -- Project Overview

We will build a **console-based movie ticket booking system** where a
user can: 1. View available movies and showtimes. 2. Choose a movie and
number of tickets. 3. Book seats (basic seat selection). 4. View total
cost. 5. Exit the program.

------------------------------------------------------------------------

## Slide 3 -- Level 1 Scope

-   **We will NOT** use advanced OOP (inheritance, polymorphism).
-   Only **basic Class & Object** usage for `Movie` and `Booking`.
-   Main logic will rely on **arrays, ArrayLists, loops, and
    conditions**.

------------------------------------------------------------------------

## Slide 4 -- Project Requirements

**Functional Requirements** 1. Display a list of movies. 2. User selects
a movie. 3. User enters number of tickets. 4. Program calculates total
cost. 5. Optional: Seat map selection.

**Non-functional** - Simple console interface. - Easy navigation.

------------------------------------------------------------------------

## Slide 5 -- Data Representation

We will store: - **Movies**: title, time, ticket price. - **Bookings**:
movie name, seats booked, total cost. - Use **ArrayList** for dynamic
booking history.

------------------------------------------------------------------------

## Slide 6 -- Example Data Structure

``` java
class Movie {
    String title;
    String time;
    double price;
}
```

We can store movies in an **ArrayList`<Movie>`{=html}**.

------------------------------------------------------------------------

## Slide 7 -- Main Menu

Example options: 1. View Movies 2. Book Ticket 3. View Booking History
4. Exit

We will use a **loop with switch-case** to handle menu choices.

------------------------------------------------------------------------

## Slide 8 -- Viewing Movies

We will display each movie in a loop:

``` java
for (int i = 0; i < movies.size(); i++) {
    System.out.println((i+1) + ". " + movies.get(i).title + " - " + movies.get(i).time);
}
```

------------------------------------------------------------------------

## Slide 9 -- Booking Tickets

Steps: 1. Ask user for movie number. 2. Ask for number of tickets. 3.
Calculate total = price × quantity. 4. Save booking in
`ArrayList<Booking>`.

------------------------------------------------------------------------

## Slide 10 -- Booking Class

``` java
class Booking {
    String movieTitle;
    int tickets;
    double totalCost;
}
```

------------------------------------------------------------------------

## Slide 11 -- Seat Selection (Optional)

We can simulate a **2D char array** for seats: - 'O' → available - 'X' →
booked

Example:

``` java
char[][] seats = new char[5][5];
```

------------------------------------------------------------------------

## Slide 12 -- Viewing Booking History

Loop through booking list:

``` java
for (Booking b : bookings) {
    System.out.println(b.movieTitle + " - " + b.tickets + " tickets - $" + b.totalCost);
}
```

------------------------------------------------------------------------

## Slide 13 -- Methods to Use

-   `displayMovies()`
-   `bookTicket()`
-   `viewBookings()`
-   `displaySeats()` (optional)

------------------------------------------------------------------------

## Slide 14 -- Control Flow Diagram

We will draw a simple flow: 1. Show menu 2. Get choice 3. Execute action
4. Repeat until exit

------------------------------------------------------------------------

## Slide 15 -- Example Main Loop

``` java
boolean running = true;
while (running) {
    displayMenu();
    int choice = sc.nextInt();
    switch (choice) {
        case 1: displayMovies(); break;
        case 2: bookTicket(); break;
        case 3: viewBookings(); break;
        case 4: running = false; break;
    }
}
```

------------------------------------------------------------------------

## Slide 16 -- Sample Output

    Welcome to Movie Booking
    1. View Movies
    2. Book Ticket
    3. View Booking History
    4. Exit
    Enter choice: 1

    Movies:
    1. Inception - 7PM - $10
    2. Titanic - 8PM - $8

------------------------------------------------------------------------

## Slide 17 -- Edge Cases

-   Invalid menu choice → show error.
-   Booking more tickets than available → reject.
-   Empty booking history → show message.

------------------------------------------------------------------------

## Slide 18 -- Testing Plan

We will test: 1. Viewing movies works correctly. 2. Booking saves
correct details. 3. Booking history displays correctly. 4. Handles
invalid inputs.

------------------------------------------------------------------------

## Slide 19 -- Student Challenge Ideas

-   Add discounts for bulk booking.
-   Add seat selection (mark seats as booked).
-   Allow movie removal (admin mode).

------------------------------------------------------------------------

## Slide 20 -- Assignment

1.  Implement the basic system.
2.  Add **at least one enhancement** from the challenges.
3.  Submit full Java source code.

------------------------------------------------------------------------

## Slide 21 -- Review

From this project we review: - Arrays & ArrayLists - Loops &
Conditions - Methods - Basic Class/Object - Input/Output handling

------------------------------------------------------------------------

## Slide 22 -- Closing

Congratulations on reaching the end of Level 1!\
This project will test your **logic, problem-solving, and code
organization**.
