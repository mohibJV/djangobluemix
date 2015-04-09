<b>djangobluemix</b>

Allows you to quickly deploy Django Python Apps To IBM Bluemix

To manually push this starter Django App to Bluemix using CF

- Modify the manifest with your file name. 
- Push the app using CF Push so you can create a service to bind to $cf push <your app name> 
- Go to Bluemix Dashboard and create your Postgres Database Service in Bluemix and bind it to your app.
- Replace your services name for your DB in manifest file
- Modify the run.sh file to create your own DJango users and password
- Push your app again using CF push.
$cf push <your app name>


To automate the deployment of this starter template Django Python Application using Deploy to Bluemix. Click the deploy to Bluemix Button.

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](http://goo.gl/UWpUya)

<b>Directions</b>
- The app will deploy however the initial application start will fail because you haven't created your postgress database service. 
- The error messages in the DevOps pipeline services shows you haven't created your postgresql-qc database service.
- Create the postgress service. I used "postgresql-qc" as the name in the manifest file.  
- Bind the service to your app in the blumix console.
- Restart your app in Bluemix
- Access the deployed app using the routesURL at the top of your app  routesURL/admin
- Use admin for user id and password and start creating users.
- Enjoy
