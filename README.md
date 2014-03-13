# tomcatPom

parental POM for Metalcon projects using Tomcat including

* WAR export plugin
* Tomcat auto deployment plugin
* Jetty server for debugging

## Use in projects

See https://github.com/Metalcon/pom/ how to use a parental pom.

### Tomcat auto deployment

To use auto deployment to your local Tomcat server you have to have Tomcat configured correctly.
There must be a server `local-tomcat` in your Maven Settings file.  
Be aware of that the credentials of this server must be set to a Tomcat user with role `manager-script`.

Set `tomcat.deploy-plugin.path` to the path for your web application:

    <project ..>
      ...
      <properties>
        <!-- Tomcat deployment path -->
        <tomcat.deploy-plugin.path>/mywebapp</tomcat.deploy-plugin.path>
      </properties>
      ...
    </project>

Use `mvn tomcat7:deploy` or `redeploy`.  
(`mvn tomcat:deploy` will result in HTTP Status message 403 for Tomcat 7 with the plugin used.)

## Versions

| Type | ArtifactId | Version | Variable |
| ---- | ---------- | ------- | -------- |
| Plugin | maven-war-plugin | 2.4 | war-plugin.version |
| Plugin | tomcat7-maven-plugin | 2.2 | tomcat.deploy-plugin.version |
| Plugin | jetty-maven-plugin | 9.1.3.v20140225 | jetty-plugin.version |
