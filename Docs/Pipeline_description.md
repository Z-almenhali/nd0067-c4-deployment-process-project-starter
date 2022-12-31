## CI/CD Pipeline
- we are using circleci for our CI/CD pipeline.
### Configuration
- The configuration in the .circleci/config.yml file.

- Frontend: Runs the script in the package.json file. Then the command in deploy.sh will run to upload the frontend asstes to S3 bucket.
- API: Runs the script in package.json. Then the command in deploy.sh will run to set the env variables to EB which are configured inside CircleCi and passed to the production application. Finally EB will upload the archive file to deploy the server by AWS CLI.