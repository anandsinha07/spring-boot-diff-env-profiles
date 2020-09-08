# Start services with specified profile
Create DBs named **demoDBdev**, **demoDBtest**, **demoDBprod** and grant all acesss to them.

## Using command line
### To start **dev** service:
```
mvn clean
mvn package -p dev
mvn spring-boot:run -P dev
```
### To start **test** service:
```
mvn clean
mvn package -p test
mvn spring-boot:run -P test
```
### To start **prod** service:
```
mvn clean
mvn package -p prod
mvn spring-boot:run -P prod
```

## Using IDE
Navigate to *application.properties* and find :
```
spring.profiles.active=@spring.profiles.active@
```
Substitute ```@spring.profiles.active@``` with *dev/test/prod* whichever service you want to use.
For eg: for dev env:
```
spring.profiles.active=dev
```
Now simply, build and run using Ctrl+R





