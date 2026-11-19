\# ShoeStop Backend



A Node.js and Express.js backend for the ShoeStop e-commerce application, integrated with MongoDB Atlas, JWT authentication, Docker, GitHub Actions, and Docker Hub.



\## 🚀 Project Overview



ShoeStop Backend provides REST APIs for managing products, users, favorites, and shopping carts.



The project is containerized using Docker and uses GitHub Actions for automated Docker image building and publishing to Docker Hub.



\## 🛠️ Technologies Used



\- Node.js

\- Express.js

\- MongoDB Atlas

\- Mongoose

\- JWT Authentication

\- Docker

\- Git \& GitHub

\- GitHub Actions

\- Docker Hub

\- Nodemon



\## 📁 Project Structure



```text

shoestop-backend/

│

├── controllers/

├── db/

├── middlewares/

├── modal/

├── routes/

├── utility/

├── .github/

│   └── workflows/

│       └── docker-build.yml

│

├── .dockerignore

├── .gitignore

├── Dockerfile

├── package.json

├── package-lock.json

├── server.js

└── README.md

```



\## 🔐 Environment Variables



Create a `.env` file in the project root:



```env

port=5000

mongoURI=YOUR\_MONGODB\_CONNECTION\_STRING

JWT\_SECRET=YOUR\_SECRET\_KEY

```



\*\*Important:\*\* Never commit `.env` to GitHub.



\## ▶️ Run Locally



Install dependencies:



```bash

npm install

```



Start the server:



```bash

npm start

```



The server runs on:



```text

http://localhost:5000

```



\## 🐳 Run Using Docker



Build the Docker image:



```bash

docker build -t shoestop-backend .

```



Run the container:



```bash

docker run -d --name shoestop-container -p 5000:5000 --env-file .env shoestop-backend

```



Check container logs:



```bash

docker logs shoestop-container

```



\## 🐳 Docker Hub



The Docker image is published to Docker Hub as:



```text

tannu1756/shoestop-backend:latest

```



Pull the image:



```bash

docker pull tannu1756/shoestop-backend:latest

```



Run the Docker Hub image:



```bash

docker run -d --name shoestop-container -p 5000:5000 --env-file .env tannu1756/shoestop-backend:latest

```



\## ⚙️ CI/CD Pipeline



The project uses GitHub Actions to automate Docker image creation and publishing.



\### Workflow



```text

Developer

&#x20;   ↓

GitHub Repository

&#x20;   ↓

GitHub Actions

&#x20;   ↓

Docker Build

&#x20;   ↓

Docker Hub

&#x20;   ↓

Docker Container

&#x20;   ↓

ShoeStop Backend

&#x20;   ↓

MongoDB Atlas

```



Whenever changes are pushed to the `main` branch, GitHub Actions:



1\. Checks out the source code.

2\. Logs in to Docker Hub.

3\. Builds the Docker image.

4\. Pushes the image to Docker Hub.



\## 🔑 Authentication



The backend uses JSON Web Tokens (JWT) for authentication.



Protected routes require an authorization header:



```text

Authorization: Bearer <token>

```



\## 📡 API Endpoints



\### User APIs



| Method | Endpoint | Description |

|---|---|---|

| POST | `/signup` | Create a new user |

| POST | `/login` | Login user |



\### Product APIs



| Method | Endpoint | Description |

|---|---|---|

| POST | `/api/addproduct` | Add a product |

| GET | `/api/getproducts` | Get all products |



\### Favorites APIs



| Method | Endpoint | Description |

|---|---|---|

| POST | `/api/addfav` | Add product to favorites |

| GET | `/api/addfav` | Get favorite products |

| DELETE | `/api/addfav/:id` | Remove favorite |



\### Cart APIs



| Method | Endpoint | Description |

|---|---|---|

| POST | `/api/addcart` | Add product to cart |

| GET | `/api/addcart` | Get cart products |

| DELETE | `/api/addcart/:id` | Remove product from cart |



\## 🧪 Testing



The Dockerized backend has been tested successfully.



Example request:



```powershell

Invoke-RestMethod -Uri "http://localhost:5000/api/getproducts" -Method Get

```



The API successfully returns product data from MongoDB Atlas.



\## 🔒 Security



Sensitive environment variables are stored locally in `.env` and excluded from Git using `.gitignore`.



Docker Hub credentials are stored securely using GitHub repository secrets.



\## 👩‍💻 Author



\*\*Tannu\*\*



B.Tech – Artificial Intelligence \& Data Science  

Rajasthan College of Engineering for Women, Jaipur

