# TripHive - Tour Booking Web App

**TripHive** is a full-stack web application for booking tour plans. It allows users to browse and book various tours, make secure payments using the Stripe payment gateway. The app is built using Node.js, Express, MongoDB, and includes essential features like user authentication, Stripe integration, and an admin panel for managing tours.

## 🎥 Demo
Check out the live demo: [TripHive Live](https://triphive-aqkd.onrender.com/)

## ✨ Features
- **User Authentication**: Sign up, login, password reset.
- **Tour Listings**: Browse and filter tours by price, ratings, and more.
- **Booking System**: Secure tour bookings with Stripe payment integration.
- **Review System**: Leave and manage reviews for tours.
- **User Dashboard**: Manage tours, and bookings.
- **Data Security**: Includes data sanitization, rate limiting, and security headers.
- **Email Notification**: Sendgrid for welcome email and forgot password emails.

## 🛠 Tech Stack

### Backend
- **Node.js**: JavaScript runtime.
- **Express.js**: Web framework.
- **MongoDB**: NoSQL database for data storage.
- **Mongoose**: MongoDB object modeling.
- **Stripe**: Payment processing.

### Module Bundler
- **Parcel**: Bundling and building assets.

### Security
- **Helmet**: Secure HTTP headers.
- **XSS-Clean**: Sanitize user input.
- **Express-Rate-Limit**: Basic rate limiting.

### Dev Tools
- **Nodemon**: Auto-restarting the server.
- **ESLint**: Code linting.
- **Prettier**: Code formatting.

## 🚀 Installation
### Prerequisites
- **Node.js** (v10 or above)
- **MongoDB** (Local or Atlas Cloud)

### Steps
1. Clone the repository:
   ```
   git clone https://github.com/Phaham/TripHive-Travel-planner.git
   cd TripHive-Travel-planner
   ```
Here is the provided content formatted in Markdown:

```
## 🚀 Installation

### Install dependencies:
```
npm install
```

### Create a `.env` file in the root directory and add the required environment variables (see [Environment Variables](#environment-variables)).

### Start the MongoDB server if you're using a local MongoDB instance:
```
mongod
```

### Build frontend assets:
```
npm run build:js
```

### Start the development server:
```
npm run dev
```

The application will be running at [http://localhost:3000](http://localhost:3000).

## 📜 Usage
1. Open the browser and navigate to [http://localhost:3000](http://localhost:3000).
2. Sign up or log in as a user.
3. Browse available tours, make bookings, and pay securely using Stripe.
4. Admin users can access the admin panel to manage tours and bookings.

## 📝 Scripts
Here are some useful commands to run during development:

| Command            | Description                                      |
|--------------------|--------------------------------------------------|
| `npm start`        | Start the server in production mode              |
| `npm run dev`      | Start the server in development mode with nodemon|
| `npm run build:js` | Build frontend assets using Parcel               |
| `npm run watch:js` | Watch for changes in frontend assets using Parcel|
| `npm run debug`    | Start the server with ndb debugger               |

## 🔧 Environment Variables
Create a `.env` file in the root of your project and add the following:

```makefile
NODE_ENV=development | production
PORT=3000
DATABASE=<your-mongodb-connection-string>
DATABASE_PASSWORD=<your-db-password>
JWT_SECRET=<your-jwt-secret>
JWT_EXPIRES_IN=no_of_days (example - 90d)
JWT_COOKIE_EXPIRES_IN=90
EMAIL_USERNAME=<your-email-username>
EMAIL_PASSWORD=<your-email-password>
EMAIL_HOST=<your-email-host>
EMAIL_PORT=<your-email-port>
STRIPE_SECRET_KEY=<your-stripe-secret-key>
```

## 📁 Folder Structure
```
TripHive-Travel-planner/
├── controllers/         # Request handlers
├── models/              # Mongoose schemas
├── public/              # Static files (CSS, JS, images)
├── routes/              # API routes
├── views/               # Pug templates
├── config/              # Configuration files
├── utils/               # Utility functions
├── app.js               # Express app setup
├── server.js            # Server startup
└── .env                 # Environment variables
```

## 📚 API Endpoints

### **Authentication**
- `POST /api/v1/users/signup` - Sign up a new user
- `POST /api/v1/users/login` - Log in a user
- `POST /api/v1/users/forgotPassword` - Request password reset

### **Tours**
- `GET /api/v1/tours` - Get all tours
- `GET /api/v1/tours/:id` - Get a tour by ID
- `POST /api/v1/tours` - Create a new tour (Admin)
- `PATCH /api/v1/tours/:id` - Update a tour (Admin)

### **Bookings**
- `POST /api/v1/bookings/checkout-session/:tourId` - Create Stripe checkout session

## 🤝 Contributing
Contributions are welcome! Please follow these steps:

1. **Fork** the project.
2. **Create** your feature branch:
   ```
   git checkout -b feature/YourFeature
   ```
3. **Commit** your changes:
   ```
   git commit -m 'Add YourFeature'
   ```
4. **Push** to the branch:
   ```
   git push origin feature/YourFeature
   ```
5. **Open a Pull Request**.
```

This Markdown format includes clear headings, syntax highlighting, and organized sections for better readability. Let me know if you need further adjustments!
