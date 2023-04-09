# ChatApplication

## Implementation Details
### Setup for Your Database
1. Create `config.yaml` in root in the format below:
```yaml
db:
  host: localhost
  port: YOUR_PORT_NUMBER
  user: USER_NAME
  password: YOUR_PASSWORD
  name: DATABASE_NAME
```
2. Excute `script/createDatabase_chatApp.sql` and `createSamples_chatApp.sql` to set up your database (MySQL)

3. Install all the dependencies:
```bash
go get "github.com/go-sql-driver/mysql"
go get "github.com/gorilla/websocket"
go get "gopkg.in/yaml.v2"
```

### Launch Server
Go to `./server` directory, run the command below:
```bash
go run main.go server.go user.go
```
### Launch Client
```bash
go run client.go handlerDatabase.go
```

## Demo

### Login Page
![Login](./imgs/login.jpg "Login")

### Register Page
![Register](./imgs/register.jpg "Register")

### Homepage (Only Public chat mode to select now)
![Homepage](./imgs/homePage.jpg "Homepage")

### Group Chat Page
![Group Chat Page](./imgs/chat_demo.jpg "Group Chat Page")

