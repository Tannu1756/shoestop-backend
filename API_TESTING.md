\# ShoeStop Backend – API Testing



\## 1. Testing Environment



\- Backend: Node.js + Express.js

\- Database: MongoDB Atlas

\- Authentication: JWT

\- Containerization: Docker

\- Container Port: 5000

\- Image: `tannu1756/shoestop-backend:latest`



\## 2. Product API



\### Get All Products



\*\*Method:\*\* GET



\*\*Endpoint:\*\*

`/api/getproducts`



\*\*Request:\*\*

```text

http://localhost:5000/api/getproducts

```



\*\*Result:\*\* Successful



The API returned product information from MongoDB Atlas.



Example response:



```json

{

&#x20; "\_id": "6afeb8e4e3ab1c0b92d1d4c6",

&#x20; "image": "https://example.com/nike.jpg",

&#x20; "company": "Nike",

&#x20; "title": "Nike Air Max",

&#x20; "price": 4999

}

```



\## 3. User Authentication APIs



\### Signup



\*\*Method:\*\* POST



\*\*Endpoint:\*\*

`/signup`



\*\*Result:\*\* Successful



A new user can be registered and an authentication token is generated.



\### Login



\*\*Method:\*\* POST



\*\*Endpoint:\*\*

`/login`



\*\*Result:\*\* Successful



Registered users can log in and receive a JWT token.



\## 4. Favorites APIs



\### Add Favorite



\*\*Method:\*\* POST



\*\*Endpoint:\*\*

`/api/addfav`



\*\*Authentication:\*\* Required



\*\*Result:\*\* Successful



\### Get Favorites



\*\*Method:\*\* GET



\*\*Endpoint:\*\*

`/api/addfav`



\*\*Authentication:\*\* Required



\*\*Result:\*\* Successful



\### Remove Favorite



\*\*Method:\*\* DELETE



\*\*Endpoint:\*\*

`/api/addfav/:id`



\*\*Result:\*\* Successful



\## 5. Cart APIs



\### Add to Cart



\*\*Method:\*\* POST



\*\*Endpoint:\*\*

`/api/addcart`



\*\*Authentication:\*\* Required



\*\*Result:\*\* Successful



\### Get Cart



\*\*Method:\*\* GET



\*\*Endpoint:\*\*

`/api/addcart`



\*\*Authentication:\*\* Required



\*\*Result:\*\* Successful



\### Remove from Cart



\*\*Method:\*\* DELETE



\*\*Endpoint:\*\*

`/api/addcart/:id`



\*\*Result:\*\* Successful



\## 6. Docker Testing



The Docker container was successfully started using the Docker Hub image:



```text

tannu1756/shoestop-backend:latest

```



Container status:



```text

Running

```



Docker logs confirmed:



```text

connected to db

server started at 5000

```



\## 7. Docker Hub Testing



The Docker image was successfully pulled using:



```bash

docker pull tannu1756/shoestop-backend:latest

```



The image was successfully downloaded and executed.



\## 8. CI/CD Testing



GitHub Actions was tested after pushing project changes.



The workflow successfully:



1\. Checked out the GitHub repository.

2\. Logged in to Docker Hub.

3\. Built the Docker image.

4\. Pushed the image to Docker Hub.



Workflow result:



\*\*SUCCESS\*\*



\## 9. Final Integration Test



The complete application flow was successfully verified:



```text

GitHub

&#x20;  ↓

GitHub Actions

&#x20;  ↓

Docker Hub

&#x20;  ↓

Docker Container

&#x20;  ↓

Node.js / Express

&#x20;  ↓

MongoDB Atlas

&#x20;  ↓

API Response

```



\## 10. Overall Testing Result



\*\*All major backend, Docker, Docker Hub, CI/CD, authentication, product, favorite, and cart functionalities were successfully tested.\*\*

