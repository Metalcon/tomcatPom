# tomcatPom

parental POM for Metalcon projects using Tomcat including

* WAR export plugin
* Tomcat auto deployment plugin
* Jetty server for debugging

## Use in projects

See https://github.com/Metalcon/pom/ how to use a parental pom.

### Tomcat auto deployment

To use auto deployment to your local Tomcat server you have to have Tomcat configured correctly.
There must be a server `local-tomcat` in your Maven Settings file and if you have set the Maven master password the password for this server **must** be encrypted.  
Be aware of that the credentials of this server must be set to a Tomcat user with role `manager-script`.

Set ${tomcat.deployPath} to the path for your web application.

    <project ..>
      ...
      <properties>
        <!-- Tomcat deployment path -->
        <tomcat.deployPath>/mywebapp</tomcat.deployPath>
      </properties>
      ...
    </project>
