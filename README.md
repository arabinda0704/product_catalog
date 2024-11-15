# product_catalog
This repo contains a product catalog site for a cake shop
# API

This is a simple Product Catalog API built with Go (Golang), using the Gin web framework and MongoDB Atlas for database storage.

## Features

- Retrieve all cakes
- Retrieve a specific cake by ID
- Add a new cake
- Delete a cake by a specific field

## Prerequisites

- Go (v1.22.6 or later)
- MongoDB Atlas account and connection URI
- Local environment file (`local.env`) for environment variables

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/goprojs/product_catalog/backend_api.git

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

1. In the root directory of your project, create a `.env` file (if it doesn’t already exist).
2. Add your MongoDB URI as follows:

```env
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/catalog?retryWrites=true&w=majority



