# Key Value Store

The key-value store is a project that allows the users to store key-value pairs in the database along with functionalities like user registration, token generation, and auth service while doing CRUD operations on the Key-value store.

## Framework, Tools, and Libraries

- **Backend**: Express JS
- **Database**: Postgres
- **ORM**: Sequelize
- **Tools and Libraries**:
  - Docker
  - bcryptjs
  - cors
  - joi
  - json web token
  - axios
  - eslint
  - nodemon

## Architecture
- The project is divided into 3 repositories,
  - **/KeyValues_auth**: Contains the Auth server, Auth DB, and Auth migration containers.
  - **/KeyValues_docker**: Contains API collection, readme, and docker-compose file to up and run all containers.
  - **/KeyValues_server**: Contains the KeyValue server, KeyVal DB, and KeyVal migration containers.
- There are 6 containers, **db_auth, db_app, keyvalues_docker-server_auth-1, keyvalues_docker-migration_app-1, keyvalues_docker-server_app-1, keyvalues_docker-migration-1**.
- 
![Architecture of containers!](/images/architecture.png "Architecture of containers")

## Setup and Run

### 1. Create a folder and inside that folder clone the below 3 repositories,
  - [https://github.com/Ashjag47/KeyValues_docker.git](https://github.com/Ashjag47/KeyValues_docker.git)
  - [https://github.com/Ashjag47/KeyValues_auth.git](https://github.com/Ashjag47/KeyValues_auth.git)
  - [https://github.com/Ashjag47/KeyValues_server.git](https://github.com/Ashjag47/KeyValues_server.git)
  - #### Example folder structure,
  - 
  ![Folder Structure!](/images/folderStructure.png "Folder Structure")
### 2. Go into the "KeyValues_docker" folder,
   ```bash
      cd KeyValues_docker
   ```
   - **To run** the entire project (all the containers),
   ```bash
      docker-compose up --build -d
   ```
   - **To stop** the entire project (all the containers),
   ```bash
      docker-compose down
   ```
### 3. API collections,
  - Here in the project [Thunder Client](https://www.thunderclient.com/) is used for API collection.
  - Install Thunder Client extension in vs code.
  - Import the API collection from "/KeyValues_docker/thunder-collection_KeyValueApi.json"
  - Use this collection to hit APIs.