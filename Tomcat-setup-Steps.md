#### Tomcat Installation Steps:

##### - JDK install it (11)

##### - Download Tomcat tar file (9.0.)

##### - Go to /opt/ and set the permissions

##### - Extract tar file to /opt folder

##### - Remove tar file after extraction is done.

##### - Rename the extracted dir to 'tomcat'

##### - Start/shut the server

##### - Verify the server

        - port (8080)
        
        - Process
        
        - URL
        
##### - Configuring manager app to access remotely

        - add the comment in TOMCAT_HOME/webapps/manager/META-INF/context.xml file
        
##### - Add the tomcat user with role in tomcat-users.xml
  
        - add the user and role in TOMCAT_HOME/conf/tomcat-users.xml file

##### - Access the manager app

        - Tomcat Server IP and port 8080
