
# Simple Supabase Authentication with TypeScript (Email + Google OAuth)

A simple and clean implementation of authentication using **Supabase** and **TypeScript**, now enhanced with **Google OAuth login**. This project demonstrates how to integrate both email/password authentication and social login via Google in a React + TypeScript app.

## ✨ Features

- 🔐 Email and Password Authentication
- 🔑 Google OAuth Authentication
- 🧠 Session Management with Supabase
- ⚛️ Built with React + TypeScript
- 🎨 Simple and customizable UI

## 🛠 Technologies Used

- **React** – Frontend library for building user interfaces
- **TypeScript** – Strongly-typed JavaScript
- **Supabase** – Open-source Firebase alternative
- **CSS** – For UI styling

## ⚙️ Prerequisites

- [Node.js](https://nodejs.org/) (v14 or later)
- npm or yarn
- A [Supabase](https://supabase.io/) project

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/james-freitas/simple-supabase-auth-typescript.git
cd simple-supabase-auth-typescript
```

### 2. Install dependencies

```bash
npm install
# or
yarn install
```

### 3. Set up Supabase

- Go to [Supabase](https://app.supabase.io/) and create a project.
- Enable **Email and Password Auth** under Authentication > Providers.
- Enable **Google Auth**:
  - Under Authentication > Settings > External OAuth Providers, enable **Google**.
  - Enter your **Google Client ID** and **Client Secret**.
  - Set up a Google project at [Google Cloud Console](https://console.developers.google.com/).
  - Use the following redirect URL:  
    `https://<your-project>.supabase.co/auth/v1/callback`

### 4. Configure Environment Variables

Create a `.env` file in the root directory:

```env
REACT_APP_SUPABASE_URL=https://your-project.supabase.co
REACT_APP_SUPABASE_ANON_KEY=your-anon-key
```

### 5. Start the development server

```bash
npm start
# or
yarn start
```

Visit `http://localhost:3000` to see the app in action.

## 🧪 How It Works

The app provides:
- Email/password signup and login
- Google login via Supabase OAuth
- Logout button
- Session tracking using React hooks (`useState`, `useEffect`)

```tsx
await supabase.auth.signInWithOAuth({ provider: 'google' });
```

Supabase redirects the user back to the app after successful authentication.

## 📁 Project Structure

```
/src
  App.tsx              # Main component with login UI and session logic
  supabaseClient.ts    # Supabase initialization
  index.tsx            # Entry point
.env                   # Environment variables
```

## 💻 UI Overview

- **Authenticated Users**: Greeting + "Sign Out" button
- **Unauthenticated Users**: Form with Email/Password, Sign Up, Sign In, and Google Login button

## 🛡 License

This project is open source and available under the [MIT License](LICENSE).

## 🙌 Acknowledgements

- [Supabase](https://supabase.io/)
- [React](https://reactjs.org/)
- [Google Developers Console](https://console.developers.google.com/)

---

> Made with ❤️ by [James Freitas](https://github.com/james-freitas)
