# Jobly

![Home page](./public/screenshots/Homepage.png "Homepage")
![log in ](./public/screenshots/Login.png "Log in")
![sign up](./public/screenshots/SignUp.png "Sign up")
![Home Page after log in](./public/screenshots/HomePage_loggedIn.png "AuthN Home Page")
![Companies List](./public/screenshots/CompaniesList.png "Companies List")
![Jobs List](./public/screenshots/JobsList.png "Jobs List")
![update Profile](./public/screenshots/updateProfileForm.png "update Profile")


Jobly is a web-based job search application that utilizes React for the front-end, an Express RESTful API for the back-end, and a PostgreSQL database for data storage. The API provides full CRUD functionality for companies, jobs, and users, with the ability to filter by custom queries. Authentication and authorization are implemented using JSON Web Tokens (JWT) for secure access to protected resources on both the front-end and back-end.



### Technologies
- React & React Router
- Axios
- Express
- JWT
- Bcrypt
- PostgreSQL
- Jest

_The backend code used in this application was provided by [Rithm School](https://www.rithmschool.com/), we built the backend as a separate exercise (code can be found [here](https://github.com/DongChoi/express-jobly)). Pair programmed with [Lynn Cha](https://github.com/lynecha) on this application._

## Available Routes

- /
- /login
- /signup
- /companies
- /companies/:handle
- /jobs
- /profile

## Main function controlling current user in app

![Code snippet - useState/useEffect](./public/screenshots/AppStateAndUseEffect.png "Code snippet - useState/useEffect")


1. Upon mounting, the application searches localStorage to retrieve any stored token to rehydrate the current user state.
2. If a token is found, it is utilized for subsequent API calls and the current user state and context is updated with information from the API. Additionally, the application interface is updated accordingly.
3. If no token is found, the login/signup buttons are displayed to prompt the user to authenticate themselves.

## Real Time filtering

- As user types in the search bar, the company and job listings are updated.