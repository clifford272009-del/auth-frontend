# AuthFrontend

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 22.3.0.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Vitest](https://vitest.dev/) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.
# Authentication & Protected Dashboard System

A full-stack user authentication application built with **Angular 21** on the frontend and **Node.js / Express / TypeScript** on the backend. It supports user registration, email verification via Ethereal/Nodemailer, login with JWT authentication, password reset, and route protection for authenticated users.

## Project Description

This project implements an end-to-end authentication and authorization workflow connecting an Angular 21 client (`http://localhost:4200`) with a Node.js/Express REST API (`http://localhost:3000`). Users can create an account, verify their email address using a preview link generated in the backend terminal during development, sign in with their credentials, reset forgotten passwords, and access a protected dashboard while unauthenticated visitors are redirected to the login page.

## Features List

- **User Registration (`/auth/register`)**: Form validation and API integration to create new user accounts.
- **Email Verification (`/auth/verify-email`)**: Generates and logs a verification email preview link via Ethereal in the backend terminal so users can verify their email address before or during onboarding.
- **User Login (`/auth/login`)**: Authenticates verified users and stores the JWT token for session persistence.
- **Password Reset (`/auth/reset-password`)**: Supports password recovery and reset flows.
- **Protected Routes & Dashboard (`/dashboard`)**: Restricts access to `/dashboard` for unauthenticated users, redirects unauthorized attempts to `/auth/login`, displays authentication status (`JWT Token stored securely`, `Email verified`, `Protected routes working`, `Automatic token attachment`), and provides a `Logout` action.
- **CORS & API Integration**: Configured Express CORS middleware to allow requests from `http://localhost:4200` with credentials enabled.

## Setup Instructions

### Prerequisites

- **Node.js** (LTS recommended) and **npm**
- **Git** (optional)
- Database configured according to your backend `src/config/data-source.ts` setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <your-project-folder>