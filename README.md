## Khoye Milgaye - Lost and Found Backend
This backend service powers the "Lost and Found" web application, which allows the university community to report lost and found items. The backend provides a RESTful API for creating, managing, and retrieving lost and found item reports. It also manages user authentication and matches lost items with found ones.

## Table of Contents
Features<br />
Tech Stack<br />
Installation and Setup<br />
API Endpoints<br />
Scripts<br />
Contributing<br />


## Features
Report Lost Items: Users can report items they have lost, providing details like category, brand, color, and the location where they lost the item.<br />
Report Found Items: Users can report found items with similar information, including the place where they found it.<br />
View Lost/Found Items: Users can view all reported lost and found items related to him.<br />
Match Lost and Found Items: The system attempts to match lost items with found items based on category, description, brand, and other factors.<br />
User Authentication: Users can register and login to the system to report and manage their lost and found items.<br />
## Tech Stack<br />
Backend:<br />
Node.js: JavaScript runtime for server-side development.<br />
Express.js: Web framework for building REST APIs.<br />
Mongoose: ODM (Object Data Modeling) library for MongoDB.<br />
JWT (JSON Web Tokens): For user authentication and authorization.<br />
Bcrypt: For password hashing and security.<br />
Database:<br />
MongoDB: NoSQL database for storing item information and user data.<br />
## Installation and Setup<br />
Prerequisites<br />
Node.js and npm installed.<br />
MongoDB installed and running.<br />
Steps to Set Up<br />
Clone the repository<br />:

bash<br />
Copy code<br />
git clone https://github.com/rajat12826/BackendLost.git <br />
cd khoye-milgaye<br />
Install dependencies:<br />

bash<br />
Copy code<br />
npm install<br />
Set up environment variables:<br />

Create a .env file at the root of the project with the following content:<br />

env<br />
Copy codve
MONGO_URI=mongodb://localhost:27017/khoyeMilgaye<br />
JWT_SECRET=your_jwt_secret_key<br />
Run the development server:<br />

bash<br />
Copy code<br />
npm start<br />
The server will run on http://localhost:5000.<br />



## API Endpoints<br />
User Routes (/api/users)<br />
POST /register: Register a new user.<br />
POST /login: Login an existing user.<br />
Lost Item Routes (/api/lostitems)<br />
POST /create: Create a new lost item report.<br />
GET /all: Retrieve all lost items.<br />
GET /:id: Retrieve a lost item by ID.<br />
Found Item Routes (/api/founditems)<br />
POST /create: Create a new found item report.<br />
GET /all: Retrieve all found items (Admin only).<br />
GET /:id: Retrieve a found item by ID (Admin only).<br />
Matching Route (/api/match)<br />
POST /match: Get matching found items for a lost item based on similarity (Authenticated users).<br />
## Scripts<br />
npm start: Start the backend server.<br />
npm test: Run tests (not yet implemented).<br />
Contributing<br />
We welcome contributions from the community. To contribute:<br />

## Fork the repository.<br />
Create a new branch for your feature or bug fix.<br />
Commit your changes.<br />
Submit a pull request.<br />
Feel free to open issues if you encounter any problems or have suggestions for improvements.<br />
