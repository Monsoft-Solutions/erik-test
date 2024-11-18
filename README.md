# Developer Test Specification for Monsoft Solutions

## Introduction

Welcome and thank you for your interest in joining **Monsoft Solutions**! To evaluate your skills and fit for our team, we have prepared a test project that mirrors the type of work you'll be engaging in. This project focuses on both client-side and server-side development, emphasizing your ability to build a functional, full-stack feature within our tech stack.

## Objective

Develop a simple CRM module that allows users to **view**, **filter**, **create**, and **update** contact data. This project will help us assess your proficiency with our technology stack, your ability to deliver clean and maintainable code, and your problem-solving skills.

## Tech Stack

Please use the following technologies and tools for this test:

- **Frontend:**
  - **Framework:** React
  - **Language:** TypeScript
  - **State Management:** Your choice (e.g., Redux, Zustand)
  - **Styling:** [Tailwind CSS](https://tailwindcss.com/) and [Radix UI](https://radix-ui.com/)
- **Backend:**
  - **Framework:** NestJS
  - **Language:** TypeScript
  - **ORM:** Drizzle
  - **Communication:** [TRPC](https://trpc.io/) using the following library versions:
    - `"@trpc/client": "^11.0.0-rc.553"`
    - `"@trpc/react-query": "^11.0.0-rc.553"`
    - `"@trpc/server": "^11.0.0-rc.553"`
- **Database:**

  - **Type:** MySQL

- **Version Control:**
  - **Repository:** GitHub (You will create a new GitHub project for this test)

## Functional Requirements

### 1. Data Model

Implement a **Contact** entity with the following fields:

- `id` (number, auto-increment, primary key)
- `firstName` (string)
- `lastName` (string)
- `email` (string, valid email format)
- `phone` (string, valid phone format)
- `company` (string)
- `position` (string)
- `status` (enum: `'New'`, `'Contacted'`, `'Qualified'`, `'Lost'`)
- `createdAt` (timestamp, auto-generated)
- `updatedAt` (timestamp, auto-updated)

### 2. Backend Features

- **API Endpoints:**

  - **Get Contacts:**

    - **Method:** GET
    - **Endpoint:** `/api/contacts`
    - **Description:** Retrieve a list of all contacts with optional filtering parameters.

  - **Create Contact:**

    - **Method:** POST
    - **Endpoint:** `/api/contacts`
    - **Description:** Add a new contact to the database.

  - **Update Contact:**
    - **Method:** PUT/PATCH
    - **Endpoint:** `/api/contacts/:id`
    - **Description:** Update an existing contact's details.

- **Filtering:**

  - Implement query parameters to filter contacts by `firstName`, `lastName`, `email`, `company`, `position`, and `status`.
  - The `status` filter should be implemented as a dropdown with the four possible values: `'New'`, `'Contacted'`, `'Qualified'`, `'Lost'`.

- **Validation:**
  - Ensure all input data is validated on the server-side (e.g., email format, required fields).

### 3. Frontend Features

- **Display Contacts:**

  - Fetch and display the list of contacts in a table format.
  - Display the following columns: First Name, Last Name, Email, Phone, Company, Position, Status.

- **Filtering:**

  - Provide input fields or dropdowns to filter contacts based on `firstName`, `lastName`, `email`, `company`, `position`, and `status`.
  - The `status` filter should be a dropdown element.
  - The table should update in real-time as filters are applied.

- **Create Contact:**

  - Provide a form or modal to input new contact details.
  - Use **Tailwind CSS** and **Radix UI** components to build the form.
  - Validate inputs on the client-side before submission.
  - Upon successful creation, the new contact should appear in the contacts table.

- **Update Contact:**

  - Allow users to edit existing contact details via inline editing or a separate form/modal.
  - Use **Tailwind CSS** and **Radix UI** components for the editing interface.
  - Validate inputs on the client-side before submission.
  - Upon successful update, the changes should reflect in the contacts table.

- **User Interface:**
  - Design a clean, intuitive, and responsive UI using **Tailwind CSS**.
  - Utilize **Radix UI** for accessible and styled UI components.
  - Ensure accessibility best practices are followed.

## Non-Functional Requirements

- **Code Quality:**

  - Write clean, readable, and maintainable code.
  - Use TypeScript effectively with proper typing and interfaces.
  - Follow best practices for both React and NestJS.

- **Documentation:**

  - Provide a comprehensive README with setup instructions, project structure overview, and any other relevant information.
  - Include database setup scripts or migration files.

- **Version Control:**

  - Use Git for version control.
  - Create a new GitHub project repository for this test.
  - Make regular, meaningful commits with clear messages.

- **Performance:**

  - Ensure the application performs efficiently with up to 100 contact records.
  - Optimize API calls and frontend rendering where applicable.

- **Error Handling:**
  - Implement graceful error handling for API failures and user input errors.
  - Provide user-friendly error messages.

## Deliverables

1. **Source Code:**

   - A GitHub repository containing the complete source code for both frontend and backend.
   - Ensure the repository is well-organized with clear folder structures.

2. **Documentation:**

   - A detailed **README** file in the GitHub repository that includes:
     - **Project Overview:** Brief description of the project.
     - **Setup Instructions:** Step-by-step guide on how to set up and run the application locally.
     - **Project Structure:** Overview of the codebase structure.
     - **Installation Steps:** How to install dependencies for both frontend and backend.
     - **Running the Application:** Commands to start the frontend and backend servers.
     - **Database Setup:** Instructions on setting up the MySQL database, including running any provided SQL scripts or migration files.
     - **Technology Stack:** List of technologies and libraries used, including versions.
     - **Assumptions:** Any assumptions made during development.
     - **Usage:** How to use the application features.
     - **Testing (Optional):** Instructions on how to run any included tests.
     - **Contact Information:** How to reach you in case of questions.

3. **Database Setup:**

   - SQL scripts or migration files using Drizzle to create the necessary database schema, including the **Contact** entity with the `status` field.

4. **Demo (Optional but Recommended):**
   - A deployed version of the application (e.g., using Vercel, Heroku) to showcase functionality.

## Timeframe

- **Total Time:** 5 Days
- **Start Date:** [Specify Start Date]
- **Submission Deadline:** [Specify End Date]

## Evaluation Criteria

Your submission will be evaluated based on the following aspects:

1. **Functionality:**

   - Completeness and correctness of the implemented features.
   - Ability to meet all the specified functional requirements.

2. **Code Quality:**

   - Cleanliness, readability, and organization of the codebase.
   - Effective use of TypeScript and adherence to best practices.

3. **Use of Tech Stack:**

   - Proper and efficient use of React, NestJS, Drizzle, TRPC (with specified versions), and MySQL.
   - Integration between frontend and backend components.

4. **User Interface:**

   - Aesthetic design and user experience.
   - Responsiveness and accessibility of the UI.
   - Effective use of **Tailwind CSS** and **Radix UI** components.

5. **Documentation:**

   - Clarity and completeness of the setup instructions.
   - Quality of inline code comments and overall documentation.

6. **Problem-Solving:**
   - Ability to handle challenges and make reasonable decisions during development.
   - Implementation of efficient and effective solutions.

## Additional Guidelines

- **Libraries and Tools:**

  - You may use additional libraries or tools if they add significant value. Please document and justify their usage in the README.

- **Assumptions:**

  - If you need to make any assumptions beyond the provided specifications, clearly state them in your documentation.

- **Testing:**

  - While not mandatory, including unit or integration tests will be considered a plus.

- **Communication:**
  - If you encounter any issues or have questions during the test period, feel free to reach out to [Your Contact Information].

## Submission Instructions

1. **GitHub Repository:**

   - Create a new GitHub repository for this test project.
   - Ensure your repository is accessible (provide access if it's private).
   - Include all necessary files and documentation as outlined in the Deliverables section.

2. **Submission:**

   - Send the GitHub repository link and any deployed demo links to [Your Email Address] by the submission deadline.

3. **Verification:**
   - Upon receiving your submission, we may reach out for a brief discussion or clarification if needed.
