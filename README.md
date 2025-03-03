# freelancer-invoice-manager
The Freelancer Invoice Manager web app will help freelancers create, manage, and track invoices for their projects. This application will feature robust user management and authentication, advanced CRUD operations for invoice data, and business logic for calculating totals, taxes, and due dates.

## Project Breakdown by Day
### Define Scope & Set Up Project

Goals:

    Define the project features and design the user flow.
    Establish the project structure and install all required dependencies.

Tasks:

    Outline core features:
        User registration, login, and session management.
        Invoice creation, editing, deletion, and viewing.
        Business logic for calculating totals, taxes, and due dates.
        Dashboard for managing and filtering invoices.
    Sketch a basic wireframe of the app (e.g., login page, dashboard, invoice form).
    Set up the project folder structure:

    /freelancer-invoice-manager
      ├── /templates        // HTML templates
      ├── /static           // CSS/JS files
      ├── main.go
      ├── routes.go
      ├── models.go
      ├── controllers.go
      └── database.go

    Initialize the project with go mod init freelancer-invoice-manager.
    Install dependencies (Gin, GORM, JWT, validator, godotenv).

📌 Deliverable: Project is initialized with a clear scope, wireframe, and folder structure.

### Set Up Database & Models

Goals:

    Design the database schema for users and invoices using GORM.

Tasks:

    Define models for:
        User: Fields include ID, Username, Email, Password (hashed), Role.
        Invoice: Fields include ID, UserID (foreign key), ClientName, Description, Amount, TaxRate, DueDate, Status, CreatedAt, and UpdatedAt.
    Write migration functions to create tables in your chosen database (SQLite for simplicity, or PostgreSQL if preferred).
    Seed the database with test data to validate relationships and data integrity.

📌 Deliverable: A fully functional database schema with working models and relationships.

### Implement User Authentication & Session Management

Goals:

    Develop secure endpoints for user registration and login.
    Protect invoice management routes with authentication.

Tasks:

    Create HTTP routes for:
        POST /register – User registration.
        POST /login – User login, returning a JWT or setting a session cookie.
    Use bcrypt to hash passwords securely.
    Implement middleware to protect invoice routes, ensuring only authenticated users can access them.
    Validate user inputs using go-playground/validator.

📌 Deliverable: A secure authentication system with protected endpoints.

### Build Backend CRUD for Invoices

Goals:

    Implement comprehensive CRUD operations for managing invoices.

Tasks:

    Develop HTTP routes for invoices using Gin:
        POST /invoices – Create a new invoice.
        GET /invoices – Retrieve all invoices for the logged-in user.
        GET /invoices/:id – Retrieve a single invoice.
        PUT /invoices/:id – Update an existing invoice.
        DELETE /invoices/:id – Delete an invoice.
    Implement business logic to calculate totals and taxes.
    Validate incoming data for each endpoint.
    Ensure proper error handling and data consistency.

📌 Deliverable: Fully functional invoice management endpoints integrated with the database.

### Build the Frontend & Connect to Backend

Goals:

    Create HTML templates for key pages and connect them to the backend API.

Tasks:

    Develop HTML templates for:
        Dashboard: Displays user invoices with filtering and sorting options.
        Invoice Form: For adding and editing invoices.
        Login/Register Pages: For user authentication.
    Use Go’s html/template to render dynamic data from the backend.
    Apply basic CSS styling (or integrate TailwindCSS/Bootstrap via CDN) for a polished look.
    Implement AJAX calls or use form submissions to connect the frontend with your API endpoints.

📌 Deliverable: A functional, interactive frontend that communicates with the backend.

### Testing, Debugging & UI Enhancements

Goals:

    Conduct thorough testing of the entire application and refine UI/UX.

Tasks:

    Manually test all functionalities:
        User registration/login.
        Invoice creation, update, deletion, and viewing.
        Business logic calculations.
    Debug any issues related to authentication, data validation, or UI rendering.
    Enhance UI elements: improve layout, add loading states, and ensure responsiveness.
    Gather feedback from potential users or peers if possible.

📌 Deliverable: A stable, bug-free application with a smooth and responsive interface.

### Final Testing, Documentation & Deployment

Goals:

    Finalize the project with comprehensive testing and documentation.
    Deploy the app to a live hosting platform.

Tasks:

    Perform end-to-end testing of all features.
    Update documentation:
        Create a detailed README including setup, usage, and deployment instructions.
        Document API endpoints and user flows.
    Use godotenv to manage environment variables (e.g., JWT secret, database URL).
    Deploy the app on a platform such as Railway, Heroku, or Fly.io.

📌 Deliverable: The Freelancer Invoice Manager is live, documented, and ready to be showcased.
