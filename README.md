## Virtual Pet Sanctuary

Virtual Pet Sanctuary is a backend application built with TypeScript, Express, and GraphQL for managing virtual pets. 

The application uses RESTful routes and supports CRUD operations for pet management, with plans for future GraphQL integration.

## Features

- Virtual pet creation, retrieval, updating, and deletion.

- JSON data parsing and in-memory storage of pet data.

- TypeScript for type safety and improved development experience.

- Planned GraphQL support for customizable data querying.

## Tech Stack

- Node.js - JavaScript runtime environment.
- TypeScript - Type-checking for JavaScript.
- Express.js - Web framework for Node.js.
- GraphQL - Query language for APIs (planned integration).
- In-Memory Data Store - Temporary data storage for pet information.

## Project Structure
```graphql
VIRTUAL-PET-SANCTUARY
├── build/                     
├── node_modules/             
├── src/                      
│   ├── server.ts             
│   ├── routes.ts              
│   ├── petData.ts             
│   ├── controller.ts          
│   ├── types.ts              
│   └── graphql/               
├── .gitignore                
├── package.json             
├── tsconfig.json             
└── README.md                 
```
**Folder explanation:** 

src/server.ts: Sets up the Express server, applies middleware, and initializes routing.

src/routes.ts: Defines RESTful endpoints for managing pet data.

src/petData.ts: Handles in-memory storage and CRUD operations for pets.

src/controller.ts: Contains controller logic for managing pet-related routes.

src/types.ts: Defines TypeScript interfaces for pet data structures.

src/graphql/: Placeholder directory for future GraphQL schema and resolvers.

## Installation and configuration

**1. Clone the repository:**

```bash
git clone https://github.com/your-username/virtual-pet-sanctuary.git
cd virtual-pet-sanctuary
```

**2. Install dependencies:**

```bash
npm install
```

**3. Compile TypeScript:**
```bash
npm run build
```
4. **Create a .env file** in the root directory based on .env.example. 
Add any necessary environment variables (e.g., PORT).

Example .env:

```plaintext
PORT=4000
```

## Usage

**1. Start the development server:**

```bash
npm run dev
```

**2.Start the production server:**

```bash
npm start
```
The server will run on http://localhost:PORT.

### Endpoints

- GET /api/pets: Fetch all pets.
- GET /api/pets/:id: Fetch a specific pet by ID.
- POST /api/pets: Create a new pet.
- PATCH /api/pets/:id: Update a pet's happiness.
- DELETE /api/pets/:id: Delete a pet.

## Example Request and Response

Create a New Pet
HTTP Method: POST
URL: /api/pets

Request Body:
```json
{
  "name": "Fluffy",
  "species": "cat",
  "color": "white",
  "size": "small",
  "happiness": 75
}
```
Expected Response:
Status: 201 Created
Response Body:

```json
{
  "id": "1",
  "name": "Fluffy",
  "species": "cat",
  "color": "white",
  "size": "small",
  "happiness": 75
}
```

