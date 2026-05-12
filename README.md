# 🚆 Train Reservation System (ORRS)

## Overview

The **Online Rail Reservation System (ORRS)** is a web-based application built with **PHP** and **MySQL** that enables passengers to search for trains, book tickets, and manage their travel — all online. The system supports three user roles: **Admin**, **Employee**, and **Passenger**, each with a dedicated portal and set of features.
---
## Live Demo

You can access the live demo of the project here:  
http://realwayreservation.great-site.net/
---

## Tech Stack

| Layer    | Technology                       |
| -------- | -------------------------------- |
| Backend  | PHP (5.6 / 7.4 / 8.1)            |
| Database | MySQL (via phpMyAdmin)           |
| Frontend | HTML, CSS, JavaScript, Bootstrap |
| Icons    | Font Awesome                     |

---

## System Roles & Features

### 👤 Passenger Portal

Passengers can register and log in to access the following features:

- **Registration & Login** — Create an account and sign in securely.
- **Train Search** — Search for available trains by route and view details.
- **Ticket Booking** — Book a seat on a selected train and receive a payment code.
- **Checkout & Confirmation** — Complete the booking with fare checkout.
- **My Booked Trains** — View all current and past reservations.
- **Ticket Cancellation** — Cancel a booked train if needed.
- **Print Ticket** — Print the confirmed ticket.
- **Profile Management** — Update personal info, change password, and upload a profile photo.
- **Password Reset** — Submit a password reset request for employee approval.

---

### 🧑‍💼 Employee Portal

Employees manage day-to-day operations of the reservation system:

- **Dashboard** — Overview of tickets, passengers, and trains.
- **Train Management** — Add, update, view, and manage train records.
- **Passenger Management** — Add and update passenger records.
- **Ticket Management** — View pending and approved tickets, confirm or reject bookings.
- **Password Reset Requests** — Approve or reject passenger password reset requests.
- **Accounting View** — View financial records related to ticket fares.
- **Profile Management** — Update personal profile, password, and avatar.

---

### 🔐 Admin Portal

The Admin has full control over the system, including all employee-level permissions plus:

- **Employee Management** — Add, update, view, and manage employee accounts.
- **Trains Management** — Add, update, view, and manage Trains.
- **Passengers Management** — Add, update, view, and manage Passengers accounts.
- **Tickets Management** — View and Manage Tickets.

---

## Database Structure

The system uses the **`orrsphp`** MySQL database with the following core tables:

| Table                 | Description                                                                 |
| --------------------- | --------------------------------------------------------------------------- |
| `orrs_admin`          | Admin account credentials and profile info                                  |
| `orrs_employee`       | Employee records including department and contact info                      |
| `orrs_passenger`      | Passenger profiles and their booked train details                           |
| `orrs_train`          | Train records: name, route, departure time, fare, and capacity              |
| `orrs_train_tickets`  | Ticket bookings with passenger info, train details, and confirmation status |
| `orrs_passwordresets` | Password reset requests with approval status (Pending / Approved)           |

---

## Key Workflows

### 🎫 Ticket Booking Flow

1. Passenger logs in → searches for available trains
2. Selects a train → books a seat
3. Proceeds to checkout → gets a unique fare payment code
4. Employee reviews and confirms the ticket
5. Passenger receives confirmation and can print the ticket

---

## Default Login Credentials

| Role     | Email             | Password      |
| -------- | ----------------- | ------------- |
| Admin    | admin@mail.com    | codeastro.com |
| Employee | employee@mail.com | codeastro.com |

---

## Project Structure

```
Train-Reservation-System/
│
├── index.php                        # Passenger landing page
├── pass-*.php                       # Passenger portal pages
├── admin/                           # Admin portal
│   ├── admin-*.php                  # Admin-specific pages
│   └── emp-*.php                    # Shared employee pages (admin access)
├── employee/                        # Employee portal
│   └── emp-*.php                    # Employee pages
├── assets/                          # CSS, JS, images
├── includes/                        # Shared includes (fonts, CSS, JS)
├── images/                          # Background and UI images
└── DATABASE FILE/
    └── orrsphp.sql                  # Full database schema + seed data
```

---
