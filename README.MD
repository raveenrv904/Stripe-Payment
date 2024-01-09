---

# Node.js Stripe Payment Processing Project

This project demonstrates the integration of Stripe payment processing in a Node.js application using Express.

## Overview

The goal of this project is to create an endpoint that handles Stripe payment intents. The `stripeController.js` file contains the logic for creating a payment intent using Stripe API, while `app.js` sets up the Express server and routes the requests.

## Prerequisites

- Node.js installed on your machine.
- Stripe account and API keys obtained from [Stripe Dashboard](https://dashboard.stripe.com/).

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:

   Create a `.env` file in the root directory and add the following:

   ```plaintext
   STRIPE_KEY=your_stripe_secret_key
   PORT=3000 # Or any other preferred port number
   ```

## Usage

1. Start the server:

   ```bash
   npm start
   ```

2. Use the `/stripe` endpoint to create a payment intent:

   Send a POST request to `http://localhost:3000/stripe` with the following JSON payload:

   ```json
   {
     "purchase": "Your Purchase Description",
     "total_amount": 1000,
     "shipping_fee": 200
   }
   ```

   Adjust the `total_amount` and `shipping_fee` values based on your requirements.

3. Upon successful creation of the payment intent, the server will respond with a JSON object containing a `clientSecret` for client-side processing.

## Project Structure

- `app.js`: Sets up the Express server, middleware, and routes.
- `controllers/stripeController.js`: Contains the logic for creating a payment intent using the Stripe API.
- `middleware/`: Contains middleware functions for error handling.
- `public/`: Directory for static files (if any).
- `package.json`: Contains project metadata and dependencies.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please create an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

---
