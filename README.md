# djangobluemix
Allows you to quickly deploy Django Python Apps To IBM Bluemix

For manually pushingt this starter Django App to Bluemix

0. Modify the manifest with your file name. 

1. Push the app using CF Push so you can create a service to bind to
$cf push <your app name>

2. Go to Bluemix Dashboard and create your Postgres Database Service in Bluemix
like postgresql-9.1 and bind it to your app.

3.Replace your services name for your DB in manifest file
applications:
- name: <your app name>
  memory: 256M
 This is command provided by cf -c option  
  command: bash ./run.sh
  buildpack: https://github.com/cloudfoundry/python-buildpack
  path: .
  services:
  - <your db service name>

4. Modify the run.sh file to create your own DJango users and password

5.Push your app again using CF push.
$cf push <your app name>