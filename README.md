https://us-east-1.console.aws.amazon.com/rds/home?region=us-east-1#database:id=database-1;is-cluster=false


https://s3.console.aws.amazon.com/s3/buckets/kouk-udagram?region=us-east-1&tab=objects

# Udagram
This application is provided to you as an alternative starter project if you do not wish to host your own code done in the previous courses of this nanodegree. The udagram application is a fairly simple application that includes all the major components of a Full-Stack web application.

## Getting Started
There's a starter project at https://github.com/Christine-M174/FullApp-HoatingProcess that
I adjusted: Added calls to scripts in package.json files, added `.env` file (see below), added scripts to
run test/deployment, added circleci configuration added docs, ...

The `.env` file needs to go into the `udagram-api` folder. It should look like
this:

POSTGRES_PORT=5432
POSTGRES_DB=database-1
POSTGRES_USERNAME=postgres
POSTGRES_PASSWORD=postgres

POSTGRES_HOST=database-1.cezjx4slfbno.us-east-1.rds.amazonaws.com
AWS_BUCKET=kouk-udagram
URL=udagram-api-dev.eba-fmzkpv6e.us-east-1.elasticbeanstalk.com

AWS_REGION=us-east-1
AWS_PROFILE=cli
AWS_ACCESS_KEY_ID=AKIAUQBNCHAUOMPCW6FR
AWS_ACCESS_KEY=AKIAUQBNCHAUOMPCW6FR
AWS_SECRET_ACCESS_KEY=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
JWT_SECRET=popopop

## Configuration documentation
- [AWS RDS](docs/config-rds.md)
- [AWS Elastic Beanstalk](docs/config-eb.md)
- [AWS S3 Buckets](docs/config-s3.md)
- [CircleCI](docs/config-circleci.md)

## Some more details on ...
- [Dependencies](/docs/dependencies.md)
- [Infrastructure](/docs/infrastructure.md)
- [Pipeline process](/docs/pipeline.md)



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

1. In AWS, provision a publicly available RDS database running Postgres. <Place holder for link to classroom article>
1. In AWS, provision a s3 bucket for hosting the uploaded files. <Place holder for tlink to classroom article>
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

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