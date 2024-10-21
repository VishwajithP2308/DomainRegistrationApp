# Domain Registration App

This is a full-stack **Domain Registration Application** built using **Next.js** and **React** on the frontend, with **Next.js API routes** on the backend to interact with GoDaddy's API for domain registration. The app allows users to search for available domain names and get domain suggestions.

## Features

- **User Authentication**: Integrated with **NextAuth.js** using Google OAuth for user authentication and session management.
- **Domain Search**: Allows users to search for domain names and checks for their availability using **GoDaddy's API**.
- **Domain Suggestions**: Provides alternative domain name suggestions if the searched domain is unavailable.
- **Form Validation**: **Formik** is used to manage form state, and **Yup** for validating domain name input.
- **API Routes**: Backend API routes are handled securely using **Next.js** to interact with GoDaddy’s API.
- **State Management and Data Fetching**: Centralized server-side state management using **React Query**, which improves scalability by managing data fetching, caching, and synchronization efficiently.
- **UI**: Built using **Chakra UI** for a clean and responsive design, making the application visually appealing and consistent.
- **Reusable Components**: Includes reusable components such as `CardLoader` and `AddDomainCard` for modular code and better maintainability.

## Tech Stack

- **Frontend**: 
  - **Next.js** (React framework for SSR and frontend logic)
  - **Chakra UI** (for UI components)
  - **Formik** (for form handling)
  - **Yup** (for form validation)

- **Backend**:
  - **Next.js API Routes** (server-side logic)
  - **Axios** (for API calls to GoDaddy’s API)
  - **NextAuth.js** (for authentication using Google OAuth)
  
- **State Management**: 
  - **React Query** (for handling server-side state, data fetching, and caching)

- **Database**: 
  - No traditional database is used in this app as it directly interacts with GoDaddy's API.
  - To mimic a backend during development, run '''npm run db''' which starts a JSON server. The JSON server acts as a mock backend,         allowing the app to function as if it had a real database.


## How it Works

1. Users log in using Google OAuth.
2. Users can search for a domain name in the search bar.
3. The app checks the availability of the entered domain by sending a request to GoDaddy’s API.
4. If the domain is unavailable, it provides alternative suggestions.
5. Users can add the domain to their cart (simulated).

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/VishwajithP2308/DomainRegistrationApp.git
   ```

2. Install the dependencies:

   ```bash
   cd DomainRegistrationApp
   npm install
   ```

3. Create a `.env.local` file and add your GoDaddy API Key, Secret, and Google OAuth credentials for NextAuth:

   ```
   GODADDY_API_KEY=your_godaddy_api_key
   GODADDY_API_SECRET=your_godaddy_api_secret
   NEXTAUTH_SECRET=your_nextauth_secret
   NEXTAUTH_URL=http://localhost:3000
   GOOGLE_CLIENT_ID=your_google_client_id
   GOOGLE_CLIENT_SECRET=your_google_client_secret
   ```

4. Run the development server:

   ```bash
   npm run dev
   ```

5. Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## Usage

- Search for a domain name using the search bar.
- If available, the domain will be shown as available; otherwise, domain suggestions will be displayed.
- You can log in with Google to save domains to the cart.

## Future Enhancements

- Integrating a full-fledged checkout system.
- Adding payment gateways for domain purchases.
- Enhancing error handling and user feedback mechanisms.


