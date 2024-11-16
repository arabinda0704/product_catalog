# product_catalog
This repo contains a product catalog site for a cake shop
# Backend API

This is a simple Product Catalog API built with Go (Golang), using the Gin web framework and MongoDB Atlas for database storage.

## Prerequisites

- Go (v1.22.6 or later)
- MongoDB Atlas account and connection URI
- Local environment file (`local.env`) for environment variables

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/goprojs/product_catalog/backend_api.git

## Query

### 1. Get All Cakes

**Endpoint:**  
`GET /cakes`

**Example:**

   ```bash
   curl -X GET http://localhost:8080/cakes

