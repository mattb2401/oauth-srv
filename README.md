# Oauth Service
To start the oauth service. Run docker-compose up --build -d to run the container in the background.
By default the service will create a database called oauth with username of root and no password.

# To build service binary
go to the srv/ folder
run the build command
    CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o srv .


# Eureka Service discovery
On application init the application will attempt to register itself to the eureka service discovery
on ip address http://192.168.99.100:8761. If the eureka service is different you can change this
IP address. After this address is changed please rebuild the application again and re run the docker-compose
command from the root of the application

# Commands to Follow.

cd srv/
CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o srv .
cd ../
docker-compose up --build -d
