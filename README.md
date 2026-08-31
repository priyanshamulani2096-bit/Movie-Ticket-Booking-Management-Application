# Movie Ticket Booking Management Application (CineWave Entertainment)

A Movie Ticket Booking Management application designed and built on the **Pega Platform™** as part of the National Internship Program (NIP).

## 📌 Project Overview
CineWave Entertainment manages movie ticket bookings across multiple theatres and locations. This Pega application automates the booking lifecycle to eliminate manual tracking, improve staff seating visibility, and send automated email confirmations.

## 🔄 Case Lifecycle Stages
1. **Request**: Captures movie ticket details from the customer (Movie, Date, Time, Show Type, Tickets).
2. **Availability**: Verifies seat counts, checks availability status, and automatically calculates booking cost.
3. **Approval**: Captures customer confirmation before finalizing.
4. **Booking Execution**: Automatically routes standard and premium screenings to respective work queues, allocates seats, and triggers confirmation notifications.

## 🛠️ Technical Implementation Details
* **Case Type**: `Movie Ticket Request`
* **Data Objects**: `Movie` (Movie Name, Genre, Duration) and `Show` (Date, Time, Seat Capacity, Show Type, Price).
* **Calculated Fields**: `Total Cost` is dynamically calculated using the expression: `.TicketPrice * .NumberOfTickets`.
* **Routing**: Conditional queue routing to `PremiumShowQueue` and `StandardShowQueue` based on `.ShowType`.
* **SLA**: Goal of 1 day (+10 urgency) and Deadline of 2 days (+20 urgency).
* **Automated Correspondence**: System-level email notification sent dynamically upon case resolution.

## 📂 Repository Contents
* `MovieTicket_Priyanshu_Amulani.docx` - Complete project submission report with step-by-step running case evidence.
* `Blueprint_MovieTicketBooking.json` - Pega Blueprint export configuration.
