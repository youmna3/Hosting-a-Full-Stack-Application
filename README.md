# Udagram

## content

- Dependencies
- Installation
- AWS Cloud Service
- Environment Variables
- Pipeline
- CircleCi
- Testing
- Built With

### Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

### Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres.
1. In AWS, provision a s3 bucket for hosting the uploaded files.
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. From the root of the repo, navigate udagram-api folder `cd udagram/udagram-api` to install the node_modules `yarn `. After installation is done start the api in dev mode with `yarn dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd udagram/udagram-frontend ` to intall the node_modules `yarn`. After installation is done start the api in dev mode with `yarn start`.

### AWS Cloud Services

- RDS - POSTGRES_HOST: database-1.c9fjnw3qxkff.us-east-1.rds.amazonaws.com
- RDS - DB_PORT: 5432
- RDS - POSTGRES_DB: udagramm
- RDS - POSTGRES_USERNAME: postgres
- RDS - POSTGRES_PASSWORD: postgres
- s3 bucket for Frontend: http://my-363479747745-bucket.s3-website-us-east-1.amazonaws.com/home
- URL -Elastic beanStalk for Backend: udagram-api-dev.eba-5xryrfdc.us-east-1.elasticbeanstalk.com

### Environment Variables

```
- POSTGRES_USERNAME
- POSTGRES_PASSWORD
- POSTGRES_DB=
- DB_PORT= 5432
- PORT=8080
- POSTGRES_HOST
- AWS_REGION
- AWS_PROFILE=
- AWS_BUCKET
- URL
- JWT_SECRET
- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
```

## Pipeline

```
- Installing Frontend Dependencies `yarn udagram-frontend:install`
- Build Angular Frontend `yarn udagram-frontend:build`
- Deploy Frontend to S3 `yarn udagram-frontend:deploy`
- Installing Backend Dependencies `yarn udagram-api:install`
- Build Backend `yarn udagram-api:build`
- Deploy the Backend using `udagram\udagram-api\bin\deploy.sh` to Elastic Beanstalk `yarn udagram-api:deploy`
```

## CircleCi

```
- spin up enviroment
- prepare enviroment variables
- install node js
- checkout
- install yarn
- install aws CLI V2
- disable aws pager
- configure aws access key ID
- configure aws secret access key
- configure aws region
- setting up elastic beanstalk CLI
- install udagram-frontend
- build udagram-frontend
- deploy udagram-frontend
- install udagram-api
- build udagram-api
- deploy udagram-api
```

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

## License

[License](LICENSE.txt)
