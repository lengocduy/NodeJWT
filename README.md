This app demo authentication for nodeJS server with JWT and deploy with docker
1. The app route some apis whether verify for request via token or not.
2. User call "register" with user info (name + password + admin) 
    2.1 add user to database mongodb.
    2.2 get token for authentication requests after that. client <token--user> Node <token--(user info + secret key)> JWT sign(user + scret key)
3. User call "api/users" to get user list with header key "x-access-token" get from authentication previously. Client <list or error--token> NodeJS <success or failed--(token + secret)> JWT verify.
4. Deployment execute via docker-compose because the app uses multiply containers(ex: the app integrate with mongo container for persistant data). We use some commands (docker-compose up --build, docker-compose down)
