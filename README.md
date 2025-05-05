# airbnb-clone-project

## 🧑‍🤝‍🧑 Team Roles


### 🔧 Backend Developer
Responsible for server-side logic, building APIs, and integrating with the database. Ensures performance, scalability, and security of the backend.

### 💻 Frontend Developer
Designs and builds the user interface. Uses modern frameworks to ensure a responsive and dynamic user experience.

### 🗃️ Database Administrator
Manages the database schema, data consistency, and query performance. Handles backups and restores.

### 🧪 QA Engineer
Tests features, finds bugs, and ensures the product meets quality standards. Writes automated and manual test cases.

### 📋 Project Manager
Oversees project timelines, coordinates team activities, and ensures deliverables are met on schedule.

### 🎨 UI/UX Designer
Creates intuitive user flows and visual designs. Focuses on user experience, layout, and accessibility.

## 🛠️ Technology Stack

This project utilizes a modern, full-stack technology stack to simulate the development of a robust booking platform similar to Airbnb. Below is an overview of the technologies used and their purpose:

### 🌐 Django
A high-level Python web framework that encourages rapid development and clean, pragmatic design. It handles the backend logic, including routing, views, and API development.

### 🗄️ MySQL
An open-source relational database management system used to store and manage structured data, such as user accounts, listings, bookings, and reviews.

### 🔄 GraphQL
A query language for APIs that allows efficient data retrieval by enabling the client to request only the data it needs. It enhances performance and flexibility compared to RESTful APIs.

### 🔐 GitHub
Used for version control, collaboration, and source code management. Supports Git workflows and pull requests for team contributions.

### 🔃 GitHub Actions (CI/CD)
An automation tool used to set up continuous integration and continuous deployment pipelines. Ensures that code is automatically tested and deployed efficiently.

### 🐳 Docker
A containerization platform that allows the project to run in isolated environments. It simplifies development, testing, and deployment by packaging the application with all dependencies.

---


## 🧩 Database Design

The database schema is designed to reflect a real-world booking platform like Airbnb. Below are the core entities and key attributes:

### **Users**
- `id`: Unique identifier for the user  
- `name`: Full name  
- `email`: Email address (unique)  
- `password_hash`: Encrypted password  
- `role`: Guest or Host  

### **Properties**
- `id`: Unique property identifier  
- `host_id`: Foreign key referencing the User (Host)  
- `title`: Property title  
- `description`: Details about the property  
- `location`: City, region, and country  
- `price_per_night`: Price in USD  
- `available_dates`: List of available dates for booking  

### **Bookings**
- `id`: Unique booking ID  
- `user_id`: Foreign key referencing the Guest  
- `property_id`: Foreign key referencing the Property  
- `check_in`: Date  
- `check_out`: Date  
- `total_price`: Calculated price for the stay  

### **Reviews**
- `id`: Unique review ID  
- `booking_id`: Foreign key referencing the booking  
- `rating`: Star rating (1 to 5)  
- `comment`: Optional text feedback  

### **Payments**
- `id`: Unique payment ID  
- `booking_id`: Foreign key  
- `amount`: Total paid  
- `payment_method`: e.g., Card, PayPal  
- `status`: Paid, Pending, Failed  

---

## ✨ Feature Breakdown

### 1. **User Management**
Allows registration, login, profile management, and role assignment (guest or host). This is essential for personalized experiences and access control.

### 2. **Property Listing & Management**
Hosts can list properties with photos, descriptions, and pricing. Listings can be edited or removed. Guests can search and filter these listings.

### 3. **Booking System**
Users can book properties by selecting dates. The system checks availability and calculates the total cost before confirmation.

### 4. **Review System**
After a completed booking, users can leave ratings and feedback. This enhances trust and improves decision-making for future guests.

### 5. **Payment Integration**
Secure payment handling ensures users can pay for bookings via multiple methods. Payment status is recorded and linked to bookings.

---

## 🔐 API Security

To ensure the platform is secure and trustworthy, several security practices are implemented:

### **Authentication**
JWT-based authentication is used to verify user identity securely during login and API access.

### **Authorization**
Access control is applied to ensure only hosts can manage listings and only logged-in users can book or review properties.

### **Input Validation**
All inputs are validated and sanitized to prevent injection attacks (e.g., SQL injection, XSS).

### **Rate Limiting**
Rate limiting is applied to public endpoints to prevent abuse or denial-of-service attacks.

### **HTTPS**
All data transfers are encrypted using HTTPS for confidentiality.

---

## 🔄 CI/CD Pipeline

A CI/CD pipeline ensures that changes to the project are automatically tested and deployed, reducing human error and speeding up delivery.

### **Why CI/CD Matters**
- Automatically tests code before deployment  
- Detects bugs early  
- Encourages frequent commits and continuous feedback  
- Ensures faster and more reliable deployments  

### **Tools Used**
- **GitHub Actions**: Runs tests and builds automatically on every push or pull request.  
- **Docker**: Creates consistent environments for local development, testing, and deployment.  
- **Pre-commit Hooks**: Ensures code style and test rules are followed before pushing changes.  


