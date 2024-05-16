# Concert Booking Service - README

## Project Description

The Concert Booking Service is a web application designed to manage bookings for a small venue with a seating capacity of 120 seats, categorized into three price bands: Silver, Gold, and Platinum. This service allows clients to retrieve information about concerts and performers, make reservations, enquire about seat availability, and authenticate users. The service ensures that double bookings are prevented, and clients can either book all their selected seats or none at all. The system is designed to scale and handle high loads during ticket sales.

## Features

- **Concert and Performer Information**: Retrieve details about concerts and performers.
- **Seat Availability Enquiries**: Check the availability of seats and their pricing.
- **Reservation Management**: Make and manage seat reservations.
- **User Authentication**: Authenticate users to enable reservations and view personal bookings.
- **Subscription Notifications**: Subscribe to notifications about concerts and dates nearing sell-out.

## Domain Model

The domain model includes the following entities:

- **Concert**: Represents a concert event, including details and dates.
- **Performer**: Represents a performer associated with concerts.
- **User**: Represents a client of the service.
- **Reservation**: Represents a booking of one or more seats by a user for a concert on a specific date.
- **Seat**: Represents individual seats in the venue, categorized into Silver, Gold, and Platinum bands.

## Technology Stack

- **Java**
- **JAX-RS**: For developing the RESTful web services.
- **JPA**: For managing persistence and mapping the domain model to the relational database.

## RESTful API Endpoints

- **Concerts**
  - `GET /concerts`: Retrieve a list of all concerts.
  - `GET /concerts/{id}`: Retrieve detailed information about a specific concert.
- **Performers**
  - `GET /performers`: Retrieve a list of all performers.
  - `GET /performers/{id}`: Retrieve detailed information about a specific performer.
- **Seats**
  - `GET /concerts/{concertId}/seats`: Enquire about available seats for a specific concert.
- **Reservations**
  - `POST /reservations`: Make a new reservation (authenticated users only).
  - `GET /reservations/{id}`: Retrieve details of a specific reservation (authenticated users only).
- **Users**
  - `POST /users/login`: Authenticate a user.
  - `POST /users/register`: Register a new user.
- **Subscriptions**
  - `POST /subscriptions`: Subscribe to notifications for a concert/date.
