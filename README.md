
# Simple Supabase Authentication with TypeScript

A simple yet complete implementation of authentication using **Supabase** and **TypeScript**. This repository demonstrates how to integrate user authentication with Supabase for a React application, covering both **sign up**, **sign in**, and **sign out** functionalities.

## Features

- **Email and Password Authentication** with Supabase.
- **Session management** using Supabase's built-in session handling.
- Responsive and simple UI with React.
- TypeScript support for type safety.
- Easy setup and integration with Supabase.

## Technologies Used

- **React** – Frontend library for building the user interface.
- **TypeScript** – Typed JavaScript for better code quality and maintainability.
- **Supabase** – Backend-as-a-Service platform for authentication and database management.
- **CSS** – Styling for the user interface.

## Prerequisites

Before running the project, make sure you have the following installed:

- **Node.js** (v14.x or later)
- **npm** or **yarn**
- A **Supabase account** and project.

## Setup

### 1. Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/james-freitas/simple-supabase-auth-typescript.git
cd simple-supabase-auth-typescript
```

### 2. Install Dependencies

Install the required dependencies:

```bash
npm install
```

Or if you're using yarn:

```bash
yarn install
```

### 3. Set Up Supabase

1. Go to the [Supabase dashboard](https://app.supabase.io/).
2. Create a new project or use an existing one.
3. Enable **Email and Password Authentication** in the Supabase project:
   - Go to **Authentication** in the Supabase dashboard.
   - Under **Settings**, ensure **Email login** is enabled.

4. Get your **Supabase URL** and **API Key** from the Supabase project settings:
   - Go to **Settings** -> **API**.
   - Copy the `SUPABASE_URL` and `SUPABASE_ANON_KEY`.

### 4. Configure the Supabase Client

Create a `.env` file in the root directory of the project and add your Supabase credentials:

```bash
REACT_APP_SUPABASE_URL=your-supabase-url
REACT_APP_SUPABASE_ANON_KEY=your-supabase-anon-key
```

### 5. Run the Project

Now you can run the application locally:

```bash
npm start
```

Or using yarn:

```bash
yarn start
```

The app should now be running on `http://localhost:3000`.

## How It Works

The application provides a simple form for users to sign up, sign in, and sign out using their email and password. Here's how the authentication process works:

1. **Sign Up** – The user enters an email and password to register. Supabase sends a confirmation email to the user.
2. **Sign In** – The user enters the email and password to authenticate. If successful, the user's session is established.
3. **Sign Out** – The user can log out, which ends the session.

The session state is managed using React's `useState` and `useEffect` hooks. The app checks for an existing session on load, and updates the UI based on whether the user is logged in or not.

## Folder Structure

Here is the general folder structure of the project:

```
/src
  /components
    App.tsx           # Main application component
    LoginForm.tsx     # Login and Signup form component
  /styles
    styles.css        # Global styles for the app
  /supabase
    supabaseClient.ts # Supabase client configuration
  index.tsx           # Entry point for the React app
  App.css             # CSS file for styling the app
  index.css           # Global styles file
.env                  # Contains your Supabase credentials
```

## UI Components

- **App Component**: Handles the main logic for signing in, signing up, and signing out.
- **LoginForm Component**: Displays input fields for the user to input their email and password, and handles the form submission.

## Customization

You can easily modify and extend the authentication system by:

- Adding **social logins** like Google or GitHub.
- Implementing **password reset** functionality.
- Integrating the app with a **backend** to store user data.
- Styling the app to fit your branding.

## Contributing

Contributions are welcome! If you have suggestions or improvements, feel free to create a pull request or open an issue.

### How to Contribute

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to your branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- **Supabase** – The open-source alternative to Firebase.
- **React** – The frontend library used to build this application.
- **TypeScript** – Adds type safety to JavaScript, improving development experience.
