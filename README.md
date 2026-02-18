🚀 Node-JS-CRUD-API

A simple RESTful CRUD API built using Node.js, Express.js, MongoDB Atlas, and Mongoose for managing contact data. This version is fully contained in a single server.js file, making it easy to deploy.

🔧 Tech Stack

Node.js

Express.js

MongoDB Atlas

Mongoose

Dotenv

PM2 (for production deployment)

AWS EC2 (for hosting)

📌 Features

Create Contact

Get All Contacts

Get Contact by ID

Update Contact

Delete Contact

⚙️ Local Setup

Clone the repository

git clone https://github.com/Naveenkuratti/Node-JS-CRUD-API.git
cd Node-JS-CRUD-API


Install dependencies

npm install express mongoose dotenv


Create a .env file in the project root:

MONGO_URI=your_mongodb_connection_string
PORT=5000


Run the server locally

node server.js


Server will run at:

http://localhost:5000

☁️ Deployment on AWS EC2

SSH into your EC2 instance

ssh -i your-key.pem ubuntu@your-ec2-ip


Clone the project and install dependencies

git clone https://github.com/Naveenkuratti/Node-JS-CRUD-API.git
cd Node-JS-CRUD-API
npm install


Create the .env file on the EC2 instance:

MONGO_URI=your_mongodb_connection_string
PORT=5000


Install PM2 globally

sudo npm install -g pm2


Start the server with PM2

pm2 start server.js --name contacts-api
pm2 save
pm2 startup


Check logs

pm2 logs contacts-api


Access the API via the public EC2 IP:

http://<your-ec2-ip>:5000


⚠️ Make sure your AWS Security Group allows inbound traffic on port 5000.

🔗 API Endpoints
Method	Endpoint	Description
GET	/api/contacts	Get all contacts
GET	/api/contacts/:id	Get contact by ID
POST	/api/contacts	Create a contact
PUT	/api/contacts/:id	Update a contact
DELETE	/api/contacts/:id	Delete a contact
👨‍💻 Developer

Naveen Kuratti
