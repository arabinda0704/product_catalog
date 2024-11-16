
# Product Catalog

This repo contains a product catalog site for a cake shop.

## Backend API

This is a simple Product Catalog API built with Go (Golang), using the Gin web framework and MongoDB Atlas for database storage.

## Prerequisites

- Go (v1.22.6 or later)
- MongoDB Atlas account and connection URI
- Local environment file (`local.env`) for environment variables

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/goprojs/product_catalog/backend_api.git
   ```

2. Navigate to the project directory:

   ```bash
   cd backend_api
   ```

3. Set up your environment file (`local.env`) with the following content:

   ```
   MONGODB_URI=your-mongodb-atlas-uri
   ```

4. Run the application:

   ```bash
   go run main.go
   ```

## Query

### 1. Get All Cakes

**Endpoint:**  
`GET /cakes`

**Example:**

```bash
curl -X GET http://localhost:8080/cakes
```

---

### 2. Get a Cake by ID

**Endpoint:**  
`GET /cake/:id`

**Example:**

```bash
curl -X GET http://localhost:8080/cake/64afc8e9e5c8e53e857ab9a5
```

---

### 3. Add a New Cake

**Endpoint:**  
`POST /cakes`

**Request Body:**  
```json
{
  "name": "Chocolate Cake",
  "description": "Rich and moist chocolate cake",
  "price": 12.99
}
```

**Example:**

```bash
curl -X POST http://localhost:8080/cakes \
-H "Content-Type: application/json" \
-d '{"name":"Chocolate Cake", "description":"Rich and moist chocolate cake", "price":12.99}'
```

---

### 4. Delete a Cake by Field

**Endpoint:**  
`DELETE /cake`

**Query Parameters:**  
- `field` (string): The field to filter on, e.g., `name` or `id`.  
- `value` (string): The value of the field to delete.

**Example:**  

Delete a cake by name:
```bash
curl -X DELETE "http://localhost:8080/cake?field=name&value=Chocolate%20Cake"
```

Delete a cake by ObjectID:
```bash
curl -X DELETE "http://localhost:8080/cake?field=_id&value=64afc8e9e5c8e53e857ab9a5"
```

---

## Notes

- Replace example ObjectIDs with actual values from your MongoDB database.
- Use appropriate values for query parameters as per your data.

# MongoDB Atlas Connection 

This repository demonstrates connecting a Go application to MongoDB Atlas using the Gin framework and MongoDB Go Driver.

## Prerequisites

- [Go](https://golang.org/dl/) (1.22.6)
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account and cluster setup
- MongoDB Go Driver (`go.mongodb.org/mongo-driver/mongo`)

## Project Setup

### 1. Create a MongoDB Atlas Cluster

1. Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) and log in.
2. Create a new project if you haven’t already.
3. Set up a new **Cluster** in your project.
4. Configure network access to allow connections from your IP address.
5. Create a **Database User** with read and write permissions.

### 2. Get the MongoDB Connection URI

After setting up the cluster:

1. Go to **Database** in MongoDB Atlas and select **Connect** for your cluster.
2. Choose **Connect your application** and copy the **connection string** provided. It should look like this:


3. Replace `<username>`, `<password>`, and `<database>` with your actual credentials and database name.

### 3. Set Up Environment Variables
