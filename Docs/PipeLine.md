## Udagram Pipeline

#### Continuous Integration

##### Github
- The developers commit and push their code to the GitHub repository which is linked to the CircleCI platform. GitHub triggers the CircleCI platform when code is pushed to the repository.
##### CircleCI
- CircleCI reads the `.circleci/config.yml` file which tells the service what has to be done. In the case of Udagram, there is a list of sequenced jobs (Refer to PipeLine Architecture.png) as following :
- ***Building Stage*** :
1. Preparing enviroment variables.
2. Install node 14.15.
3. Checkout Github code.
4. Install frontend/backend depencencies.
5. Linting frontend.
6. front end build.
7. backend build.
- ***Deployment Stage***:
1. Preparing Enviroment variables.
2. Install node 14.15.
3. Installing Aws / AWS-EB
4. Configuring Access keys.
5. Checkout github code.
6. Deploying to both frontend/backend servers.