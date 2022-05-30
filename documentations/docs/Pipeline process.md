# CircleCi

## Pipeline

- A set of instructions that will be executed on a server with the goal of building and deploying your application

### How to use CircleCi

- create a github repo (push and commit the code to it)
- link the repo to CircleCi
- create .circleci\config.yml
- cirecleCi reads from .circleci\config.yml to do the jobs

### the order of jobs in CircleCi

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
