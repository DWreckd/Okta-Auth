# Okta Authentication Demo

This project demonstrates how to integrate Okta's authentication service into a web application using JavaScript. It provides a simple interface for users to log in and log out, displaying their authentication details upon successful login.

## Prerequisites

- An Okta developer account. You can sign up for a free account at [Okta Developer](https://developer.okta.com/).
- Node.js and npm installed on your machine (optional, for running a local server).

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd okta-auth-demo
   ```

2. **Create an Okta Application**
   - Log in to your Okta developer account.
   - Navigate to the **Applications** section and click on **Add Application**.
   - Choose **Web** as the platform and click **Next**.
   - Fill in the application settings:
     - **Login redirect URIs**: `http://localhost:9000/`
     - **Logout redirect URIs**: `http://localhost:9000/`
   - Click **Done** to create the application.
   - Note the **Client ID** and **Okta Domain** (base URL).

3. **Update the `index.html` File**
   - Open `index.html` in a text editor.
   - Replace the `appClientID` and `baseOktaURL` variables in the script with your Okta application's Client ID and Okta Domain.

4. **Run the Demo**
   - You can use a simple HTTP server to serve the `index.html` file. If you have Python installed, you can run:
     ```bash
     python -m http.server 9000
     ```
   - Open your browser and navigate to `http://localhost:9000/`.

5. **Testing the Authentication**
   - Click the "Log In" button to initiate the authentication process.
   - After logging in, you should see your user information displayed on the page.

## Troubleshooting

- Ensure that your user is assigned to the Okta application if you encounter access denied errors.
- Check the browser console for any error messages if the authentication does not work as expected.

## License

This project is licensed under the MIT License.