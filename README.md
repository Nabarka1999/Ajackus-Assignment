# User Management System

## Features
A simple yet effective system for managing user details, including the ability to add, modify, and delete user information.

## Technologies Used

### Backend:
- **Node.js**: JavaScript runtime environment for building scalable applications.
- **Express.js**: Web framework for Node.js, providing a robust set of features to develop APIs.
- **MongoDB**: NoSQL database for storing user data, providing flexibility and scalability.

### Frontend:
- **React.js**: JavaScript library for building user interfaces.
- **CSS**: Styling the application with a focus on a clean and responsive design.

## Challenges Faced & Solutions

### 1. **ID Numbering of Users**
   - **Challenge**: The default ID generated by MongoDB was a long string, which lacked clarity and consistency when displaying user IDs.
   - **Solution**: I implemented a counter schema to track user IDs in a sequential manner, ensuring that each user gets a clean, ordered ID, making it more user-friendly and easier to follow.

### 2. **Pagination**
   - **Challenge**: Implementing pagination to display user data in chunks (10 users per page) was tricky. Managing large datasets and ensuring the correct users were displayed on each page required additional logic.
   - **Solution**: I implemented pagination by leveraging React’s state management (currentPage and usersPerPage). This allowed dynamic adjustment of the displayed users based on the selected page and ensured smooth navigation between pages.

### 3. **Integrating Frontend with Backend API**
   - **Challenge**: Ensuring smooth integration between the frontend and backend, especially when fetching and updating user data. Handling asynchronous operations like adding, editing, and deleting users often led to inconsistent states or data not being refreshed as expected.
   - **Solution**: I used **axios** for handling API requests and ensured state updates were properly managed after every operation (fetching, adding, editing, or deleting users). This allowed the frontend to reflect the latest changes from the backend without issues.

## Running the Application

### Prerequisites:
1. **Fork this repository** and clone it to your local machine.
2. **Install Dependencies**:
   - Run `npm install` in both the frontend and backend directories to install required node modules.
   - Check the dependencies and devDependencies sections in the package.json file to ensure all required packages are listed.

### Backend Configuration:
1. In the `config.js` file in the backend folder, update the MongoDB connection string to match your MongoDB instance.
2. Ensure that the backend server is running on the desired port. Update the port number if necessary in the backend configuration file (e.g., `server.js` or `app.js`).

### Frontend Configuration:
1. In the frontend directory, make sure the API endpoint URL matches the backend API. You may need to adjust the `apiUrl` if the backend server is running on a different port or domain.



