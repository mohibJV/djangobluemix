##djangobluemix

Allows you to quickly start building and deploying Django Python Apps To IBM Bluemix.

##To manually push this starter Django App to Bluemix using CF

# Getting Started

1. Create a Bluemix Account

    [Sign up][sign_up] in Bluemix, or use an existing account. Watson Services in Beta are free to use.

2. Download and install the [Cloud-foundry CLI][cloud_foundry] tool

3. Edit the `manifest.yml` file and change the `<application-name>` to something unique and modify the services name to reflect your own Postgres SQL database service instance on Bluemix after you create it.
  ```none
  applications:
  - name: personality-insights-python
    command: python server.py
    path: .
    memory: 256M
    services:
    - personality-insights-service
  ```

    The name you use will determinate your application url initially, e.g. `<application-name>.mybluemix.net`.

4. Connect to Bluemix in the command line tool
  ```sh
  $ cf api https://api.ng.bluemix.net
  $ cf login -u <your user ID>
  ```

5. Create the PostGress Databse Service on in Bluemix

  ```sh
  $ cf create-service postgresql "100" postgresqlmine
  ```

6. Push it live!

  ```sh
  $ cf push
  ```

## To automate the deployment of this starter template 
Simply click on the deploy to bluemix button below to deploy this Django Python Application. 

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](http://goo.gl/UWpUya)

<b>Directions</b>
- Accept the default values for you the app location and name. 
- The app will deploy however the initial application start will fail because you haven't created your postgress database service.  See steps above on how to create a db service.
- The error messages in the DevOps pipeline services shows you haven't created your postgresql-qc database service.
- Create the postgress service. I used "postgresql-qc" as the name in the manifest file.  
- Bind the service to your app in the blumix console.
- Restart your app in Bluemix
- Access the deployed app using the routesURL at the top of your app  routesURL/admin
- Use admin for user id and password and start creating users.
- Enjoy

## Troubleshooting

To troubleshoot your Bluemix app the main useful source of information are the logs, to see them, run:

  ```sh
  $ cf logs <application-name> --recent
  ```

## License

  This sample code is licensed under Apache 2.0. Full license text is available in [LICENSE](LICENSE).

## Contributing

  See [CONTRIBUTING](CONTRIBUTING.md).

