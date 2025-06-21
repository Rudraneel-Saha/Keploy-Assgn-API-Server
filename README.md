📚 Book Library API
A simple RESTful API server for managing a book library, built with Node.js, Express, and MongoDB.

🚀 Features
Create, Read, Update, and Delete (CRUD) books

MongoDB database integration

RESTful API design

Easy to extend and integrate with any frontend

🛠️ Tech Stack
Backend: Node.js, Express.js

Database: MongoDB, Mongoose

API Format: JSON

📦 Installation
Clone the repository

bash
git clone https://github.com/your-username/book-library-api.git
cd book-library-api
Install dependencies

bash
npm install
Start MongoDB

Make sure MongoDB is running locally (mongod in a separate terminal).

Start the server

bash
node server.js
Or, for auto-reload on changes:

bash
npx nodemon server.js
📝 API Endpoints
Method	Endpoint	Description
GET	/api/books	Get all books
GET	/api/books/:id	Get book by ID
POST	/api/books	Add a new book
PUT	/api/books/:id	Update a book
DELETE	/api/books/:id	Delete a book
📖 Sample Book Object
json
{
  "title": "1984",
  "author": "George Orwell",
  "published_year": 1949,
  "genre": "Dystopian"
}
🧪 Example Requests
Add a Book
bash
curl -X POST http://localhost:5000/api/books \
-H "Content-Type: application/json" \
-d '{"title":"1984","author":"George Orwell","published_year":1949,"genre":"Dystopian"}'
Get All Books
bash
curl http://localhost:5000/api/books
Update a Book
bash
curl -X PUT http://localhost:5000/api/books/<book_id> \
-H "Content-Type: application/json" \
-d '{"genre":"Classic"}'
Delete a Book
bash
curl -X DELETE http://localhost:5000/api/books/<book_id>
⚙️ Project Structure
text
book-library-api/
├── models/
│   └── Book.js
├── routes/
│   └── books.js
├── server.js
├── package.json
└── README.md
🗄️ Database
Uses MongoDB.

Default connection string: mongodb://localhost:27017/booklibrary

Change the connection string in server.js if needed.

💡 How to Run
Install dependencies: npm install

Start MongoDB: mongod

Start the server: node server.js or npx nodemon server.js

Use Postman, curl, or your frontend to interact with the API

