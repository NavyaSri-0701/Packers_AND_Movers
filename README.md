# Packers and Movers Website

This project is a web application that allows users to search for Packers and Movers companies based on their 'from' and 'to' locations. It provides detailed company information, cost estimates, and allows users to book orders online. The system also includes an admin panel to manage transactions and company listings.

## Features

- User Registration & Login:  
  Users can register and log in to view available services and book moving services.

- **Company Listings**:  
  Users can browse Packers and Movers companies based on their selected 'from' and 'to' locations, with details on costs, ratings, and contact information.

- Cost Estimation:  
  Approximate costs are displayed based on the distance between the selected cities, with the ability to adjust pricing for different routes. For same-location moves, a fixed cost of ₹6000 is applied.

- Booking:  
  Users can book a service with the selected company and receive a confirmation. 

- Admin Panel:  
  Admins have access to a dedicated panel where they can manage company listings, approve or cancel transactions, and update company details in real-time.

## Benefits

- Easy Search and Book:  
  Users can quickly find moving companies, compare costs, and make bookings all from one place.

- Accurate Cost Predictions:  
  The system provides cost estimates based on actual distances between cities, offering transparency in pricing.

- Real-Time Transaction Management:  
  Admins can manage bookings, track user requests, and update the database instantly.

## Technologies Used

- Frontend: HTML, CSS, Bootstrap 4.5.2
- Backend: JSP (Java Server Pages)
- Database: MySQL
- Web Server: Apache Tomcat (or any compatible server)

## Database Structure

### Tables

1. userdata:
   - `id`: Integer (Primary Key)
   - `username`: VARCHAR
   - `email`: VARCHAR
   - `password`: VARCHAR

2. companies:
   - `id`: Integer (Primary Key)
   - `company_name`: VARCHAR
   - `cost_per_km`: Integer (Cost in INR)
   - `phone_number`: VARCHAR (Indian format: +91 XXXXXXXXXX)
   - `rating`: Float (Scale from 1 to 5)
   - `from_location`: VARCHAR
   - `to_location`: VARCHAR

### Cost Logic

- Same 'from' and 'to' locations: ₹6000
- For different city pairs**: Costs are more than ₹5000 for shorter distances and over ₹15000 for longer routes, based on Indian geography.
- You can change the costs.

### Sample Data

The sample data includes entries for Packers and Movers companies covering routes between major Indian cities (Delhi, Mumbai, Bangalore, Hyderabad, Chennai, and Kolkata). The data includes company names, cost per kilometer, phone numbers, and ratings.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/packers-and-movers.git
   cd packers-and-movers
