# OIDC State Issue

To reproduce the issue do the following:

1) Verify Docker environment is available for OIDC Dev Service.
2) Start application using `./mvnw quarkus:dev`
3) Open [http://localhost:8080](http://localhost:8080)
4) Login using joe/anonymous 
5) Click logout
6) Login using joe/anonymous

Once you log in for the second time you get the ?state=.... parameter which should not be there as it isn't there
the first time.