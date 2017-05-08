[![logo](http://www.tango-controls.org/static/tango/img/logo_tangocontrols.png)](http://www.tango-controls.org)

This project is an attempt to implement Tango Controls Roadmap [Feature Request #6](http://www.tango-controls.org/community/roadmap/)

## Live demo

Watch this app running on Amazon cloud: [link](http://ec2-52-59-200-167.eu-central-1.compute.amazonaws.com:8080/TangoWebapp/)

User: tango-cs
Pass: tango

## Requirements ##

* Tango Controls environment (tested on Tango 8 and Tango 9)
* Tango REST Server that supports API spec version at least rc3 (tested on mtango.server-rc3-0.1)
* Web server that can handle .war files (tested on Apache Tomcat 8)

## Getting started ##

1. Download [TangoWebapp.war](https://github.com/Ingvord/tango-webapp/releases/download/0.1/TangoWebapp.war) file.
2. Copy it into your webserver's web applications root folder, e.g. {CATALINA_HOME}/webapps
3. Define a tomcat user who has the role "mtango-rest".
4. Restart server
5. Open browser and navigate to <your_host>/TangoWebapp
6. Adjust TANGO_REST_URL (must point to a valid Tango REST server, e.g. `http://{host}:{port}/tango/rest`) and TANGO_HOST values in the left top corner of the app
7. Press refresh button
8. Explore your Tango devices...

## Build ##

This project uses gradle for high level build operations. Supported tasks are:

```
Build tasks
-----------
clean - Deletes the build directory.
prepareBuild - creates build's skeleton
compress - compresses JavaScript
prepareWar - archives build into a .war file
deploy - deploys generated .war file to the downloads page 
```

## Implementation details ##

* [JavaScriptMVC-1.5.x](https://bitbucket.org/Ingvord/javascriptmvc-1.5.x) is used for MVC implementation
* [Webix-3.4](http://webix.com) is used for UI
