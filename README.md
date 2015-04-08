djangobluemix

Allows you to quickly deploy Django Python Apps To IBM Bluemix

For manually pushingt this starter Django App to Bluemix

1. Modify the manifest with your file name. 

2. Push the app using CF Push so you can create a service to bind to
$cf push <your app name>

3. Go to Bluemix Dashboard and create your Postgres Database Service in Bluemix
like postgresql-9.1 and bind it to your app.

4.Replace your services name for your DB in manifest file

5. Modify the run.sh file to create your own DJango users and password

6.Push your app again using CF push.
$cf push <your app name>


For automating the deployment of this starter template Django Python Application to Bluemix. Click the deploy to Bluemix Button.

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=http://goo.gl/mXgcwK)
