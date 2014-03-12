# tomcatPom

parental POM for Metalcon projects using Tomcat including

* WAR export plugin
* Tomcat auto deployment plugin
* Jetty server for debugging

## Use in projects

See https://github.com/Metalcon/pom/ how to use a parental pom.

### Tomcat auto deployment

To use auto deployment to your local Tomcat server you have to have Tomcat configured correctly.
The server id is `local-tomcat`.  
Be aware of that the credentials of this server must be set to a user with role `manager-script`.
