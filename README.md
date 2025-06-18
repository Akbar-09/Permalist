# Todo List App

Permalist website it's a permanent to-do list you can't lose your to-do list info anymore. It provides multiple to-do lists for Today, this Week, and this Month. Because some tasks can't be done in one day, some might take a week or a month.


# Features

- Add new items to the list
- Edit existing items
- Delete items
- View all items in the list
- *New*: Add Daily, Monthly, Yearly lists. You can add tasks that need to be completed.  


# Technologies Used

- Node.js
- Express
- PostgreSQL
- EJS (Embedded JavaScript) templates
- Body-parser middleware


## Prerequisites

- Node.js installed
- PostgreSQL installed


## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Akbar-09/permalist.git
   ```

2. Navigate to the project directory:

   ```bash
   cd your_repository
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Set up PostgreSQL database:

   - Create a new database named `permalist`.
   - Run the SQL script `schema.sql` in the repository to create the necessary table.


5. Configure database connection:

   -  Delete this part of the code it is the DB connection inside index.js file:

```javascript

const db = new pg.Client({
  connectionString: process.env.DATABASE_URL,
});
```

- Replace it with this inside index.js:
```javascript
const db = new pg.Client({
  user: 'your_database_user',
  host: 'your_database_host',
  database: 'your_database_name', // For example permalist
  password: 'your_database_password',
  port: your_database_port,
});
```

## Usage

1. Start the server:

   ```bash
   npm start
   ```

2. Open your web browser and navigate to `http://localhost:3000` to access the application.

3. Use the application to create, edit, and delete tasks on your to-do list.

## Acknowledgments

This project is inspired by the need for a simple and efficient way to manage tasks and is provided for educational purposes.
