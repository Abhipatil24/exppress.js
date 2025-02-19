# Tea Management CRUD API  

This is a simple REST API built with **Node.js** and **Express** to manage a collection of teas. It allows users to **Create, Read, Update, and Delete (CRUD)** tea records.

## Features  
- **Add a new tea**  
- **Get all teas**  
- **Get a tea by ID**  
- **Update tea details**  
- **Delete a tea**  

## Technologies Used  
- **Node.js**  
- **Express.js**  

## Installation  

1. **Clone the repository**  
   ```sh
   git clone https://github.com/your-username/tea-management.git
   cd tea-management
   ```
2. **Install dependencies**  
   ```sh
   npm install
   ```
3. **Run the server**  
   ```sh
   node index.js
   ```
   Or, if using **nodemon** (recommended):  
   ```sh
   npx nodemon index.js
   ```

## API Endpoints  

### 1. Create a Tea  
**Endpoint:** `POST /teas`  
**Request Body:**  
```json
{
  "name": "Green Tea",
  "price": 50
}
```  
**Response:**  
```json
{
  "id": 1,
  "name": "Green Tea",
  "price": 50
}
```

### 2. Get All Teas  
**Endpoint:** `GET /teas`  
**Response:**  
```json
[
  {
    "id": 1,
    "name": "Green Tea",
    "price": 50
  }
]
```

### 3. Get a Tea by ID  
**Endpoint:** `GET /teas/:id`  
**Response (if found):**  
```json
{
  "id": 1,
  "name": "Green Tea",
  "price": 50
}
```
**Response (if not found):**  
```json
"tea is not found..."
```

### 4. Update a Tea  
**Endpoint:** `PUT /teas/:id`  
**Request Body:**  
```json
{
  "name": "Black Tea",
  "price": 60
}
```
**Response:**  
```json
{
  "id": 1,
  "name": "Black Tea",
  "price": 60
}
```

### 5. Delete a Tea  
**Endpoint:** `DELETE /teas/:id`  
**Response (if found and deleted):**  
```json
"deleted"
```
**Response (if not found):**  
```json
"tea not found"
```

## Notes  
- Ensure `Node.js` and `npm` are installed.  
- This project uses an **in-memory** array (`teaData`), meaning data resets when the server restarts.  
- Consider using **MongoDB** or **PostgreSQL** for persistent storage in the future.  

## License  
This project is open-source and free to use.

