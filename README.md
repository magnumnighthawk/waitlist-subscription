# Ticket Waiting List Application

This application simulates a waiting list system for event tickets, allowing users to sign up to be notified when more tickets become available after an initial sell-out. It's designed to mimic the core functionality found on platforms like Ticketmaster, providing a simple and effective way for fans to express interest and potentially secure tickets.

## Key Features

- **Waiting List Form:** A user-friendly form that collects the fan's email address and mobile number.
- **API Integration:** Submits user data via a POST request to a `/api/waiting-list` endpoint (simulated in this example).
- **Success/Error Handling:** Displays clear success messages upon successful submission and error messages if the API request fails.
- **Loading State:** Provides visual feedback during the submission process, indicating to the user that their request is being processed.
- **Accessibility:** Built with accessibility in mind, ensuring usability for all users.
- **Basic Styling:** The design is inspired by the Ticketmaster website, giving it a familiar look and feel.
- **Form Validation:** implemented basic form validation to ensure required fields are filled.
- **Unit Tests:** Includes unit tests for improved code quality and reliability.

## Project Structure

The project is structured as a Next.js application. Key directories and files include:

- `pages/`: Contains the main pages of the application, including:
  - `index.js`: The landing page, displaying a "No seats available" notice.
  - `waiting-list.js`: The form page where users can join the waiting list.
  - `api/waiting-list.js`: simulated api that gets called.
- `components/`: Contains reusable UI components:
  - `Form.js`: The waitlist form component.
  - `LoadingSpinner.js`: Loading spinner component.
  - `ErrorMessage.js`: component for error messages.
  - `SuccessMessage.js`: component for success messages.
- `public`: includes static files like images.
- `tests`: includes unit tests.
- `package.json`: Contains project dependencies and scripts.
- `README.md`: This file!

## Getting Started

Follow these steps to set up and run the application on your local machine:

### Prerequisites

- **Node.js:** Make sure you have Node.js (version 14 or later recommended) installed. You can check by running `node -v` in your terminal.
- **Yarn:** This project uses Yarn as the package manager. If you don't have it, install it globally: `npm install -g yarn`

### Installation

1.  **Clone the repository:**
    ```bash
    git clone <repository-url> # replace with the actual URL if available, otherwise, create a repository and initilize git
    cd waitlist-subscription
    ```

2.  **Install dependencies:**
    ```bash
    yarn install
    ```

### Running the Application

1.  **Start the development server:**
    ```bash
    yarn dev
    ```
    This will start the Next.js development server, and you can access the application in your browser at `http://localhost:3000`.

2.  **Build for production:**
    ```bash
    yarn build
    ```
    This command will create an optimized production build of your application in the `.next` directory.

3.  **Start in production mode:**
    ```bash
    yarn start
    ```
    This will serve the production build of your application.

### Running Tests

To run the tests:
```bash
yarn test
```

## Notes on Design Choices

- **Next.js:** The project leverages Next.js for its built-in features like routing and server-side rendering (SSR) capabilities, though not heavily utilized here.
- **Styled Components:** It is suggested that we use styled-components, but it was not a requirement.
- **Accessibility:** Focus has been put on using semantic HTML, ARIA attributes (where needed), and good color contrast to improve accessibility.
- **Validation:** Basic validation is implemnted to ensure the required fields are filled.
- **Testing:** Uses Jest to write and run unit tests for the components.

## Further Development

- **Database Integration:** Integrate a real database to store waiting list submissions.
- **Email/SMS Notifications:** Set up a system to send email or SMS notifications when tickets become available.
- **Enhanced Validation:** Implement more comprehensive form validation (e.g., email format, phone number format).
- **Advanced Styling:** Refine the styling and UI to match the Ticketmaster website more closely.
- **Comprehensive Testing:** Add integration or end-to-end tests.

## Changelog

- **V2:**

  - Added level 1 headings to the markdown.
  - Replaced `react-helmet` with `next/head` and added `\_document.js` for better header management.
  - Added `alert` role to success messages.

- **Initial:**
  - Added 2 pages: Landing page ("No seats available") and Join Waitlist page.
  - Created components that make up the pages.
  - Implemented success & error states for waitlist submissions.
  - Added a loading state for the form submission.
  - Added unit tests.
  - Added basic form validation.

---

This project serves as a basic foundation for a more robust ticket waiting list application. Please feel free to provide feedback or suggest improvements!
