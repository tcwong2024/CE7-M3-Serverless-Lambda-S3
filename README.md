# Create serverless lambda function to convert csv file into txt file format and the input and output fille will store in S3 bucket seperatly.

1. Create and clone new github repository.
2. Add the "serverless-lambda-s3" folder inside the local git folder. 
3. Locate to serverless-lambda-s3 folder and edit the serverless.yml. modify below setting
    ```
       - service: wtc-serverless-lambda-s3
       - runtime: nodejs20.x 
       - region: us-east-1
       - name: wtcProcessCSV
       - bucket: wtc-serverless-bucket-input
       - BucketName: wtc-serverless-bucket-output
    ```
   
4. Setup the package and dependency
     ```
       - npm install -g serverless
       - npm install
       - npm ci
     ```
5. To deploy serverless into AWS run below command
   ```
       - serverless deploy -v
   ```
6. Clean up
    - S3 Bucket - manually delete the file in S3 bucket
    - Serverless 
   ```
       - serverless remove
   ```  

