# Starting with Serverless configuration and deploying to AWS Lambda with returning in url "Hello World" 🚀

## ✔ Step by Step ✔
- Install framework serverless on your pc global, or in your project 
    => npm install serverless -g  
    => npm install serverless 

- We will create the serverless project and template 
    => serverless create --template aws-nodejs
        -> After that, the serverless structure will be created in your project
            -  Follow the serverless.yml template with settings

- Create an account on AWS to be able to deploy by uploading to AWS services
    => https://aws.amazon.com/pt/console/

- After that, we will config the Service credentials to one user
        -> With an account created on AWS, we will enter the IAM (Identity and Access Management) service.
            - click in Users
            - create users
            - create name user -> next
            - Attach polices directly -> select: AdministratorAccess -> next
            - create user
        -> Enter to the created user panel
            - create access key
            - select Application running on an AWS compute service -> next
            - create description -> click in create access key
            - It will look like the access keys and the secret access key.
        -> With these keys you will configure your credentials in your project
            - Open your terminal and type following command
                -> serverless config credentials --provider aws --key=access key --secret access key secret -o
            - Command above will run and configure your credentials
        -> Then we will execute the deploy command
            - In your terminal, run the following command:
                -> serverless deploy
            - With this command, the url of your function will be generated.
                -> example ulr generated: https://example-example-sua-api.us-east-1.amazonaws.com/heloWord
