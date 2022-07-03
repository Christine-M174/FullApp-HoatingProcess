# Infrastructure Description

![Architecture](architecture_diagram.png)

## Dependencies
- AWS RDS
- AWS Elastic Beanstalk (EB)
- AWS S3

## Description
- The user connects to the frontend in an S3 bucket (frontend).
- The frontend sends get requests to the backend on EB in order to fetch existing posts.
- The frontend sends post requests to the backend on EB in order register or login the user and to add posts.
- The backend stores data to and retrieves data from a postgres RDS.
- The backend stores images in an S3 bucket (images).
- The backend sends data to the frontend.
- The S3 bucket (frontend) fetches images from the S3 bucket (images) based in the URL inside the data that was sent by the backend.
Project Infrastructure consists of three main components as shown in above figure:

1. AWS RDS Postgres: database to store and retrieve data 

   Endpoint: ``` database-1.cezjx4slfbno.us-east-1.rds.amazonaws.com ```

2. AWS Elastic Beanstalk: acts as a srever

    URL: ``` udagram-api-dev.eba-fmzkpv6e.us-east-1.elasticbeanstalk.com```

3. AWS S3: for static files storage (like frontend files)
    * Endusers can access the application through S3 Bucket.
    * URL:  http://kouk-udagram.s3-website-us-east-1.amazonaws.com 
