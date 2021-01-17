# Tutorial :

- https://aws.amazon.com/getting-started/hands-on/build-react-app-amplify-graphql

## amplify.yml :

- https://docs.aws.amazon.com/amplify/latest/userguide/build-settings.html

## Amplify Backend :

```sh
--------------------------------------------
# Amplify Backend Admin UI Local Setup:

$ amplify pull --appId d29td19f3gtnea --envName staging
Opening link: https://ap-south-1.admin.amplifyapp.com/admin/d29td19f3gtnea/staging/verify/
✔ Successfully received Amplify Admin tokens.
Amplify AppID found: d29td19f3gtnea. Amplify App name is: aws-amplify-react-app
Backend environment staging found in Amplify Console app: aws-amplify-react-app
? Choose your default editor: Visual Studio Code
? Choose the type of app that you,re building javascript
Please tell us about your project
? What javascript framework are you using react
? Source Directory Path:  src
? Distribution Directory Path: build
? Build Command:  npm run-script build
? Start Command: npm run-script start
? Do you plan on modifying this backend? Yes
✔ Successfully pulled backend environment staging from the cloud.


Successfully pulled backend environment staging from the cloud.
Run 'amplify pull' to sync upstream changes.

--------------------------------------------
# Open Amplify Admin UI:

$ amplify console
✔ Which site do you want to open? · Admin
https://ap-south-1.admin.amplifyapp.com/admin/d29td19f3gtnea/staging/home

# Open Amplify Console:

$ amplify console
✔ Which site do you want to open? · Console
https://ap-south-1.console.aws.amazon.com/amplify/home?region=ap-south-1#/d29td19f3gtnea/YmFja2VuZA/staging

# Root Cloudformation Stack for Amplify Backend:
# amplify-amplifybce972215ef64-staging-25332

--------------------------------------------
# Add Amplify Libraries:

$ yarn add aws-amplify @aws-amplify/ui-react

# Create the authentication service:

$ amplify add auth
Using service: Cognito, provided by: awscloudformation

 The current configured provider is Amazon Cognito.

 Do you want to use the default authentication and security configuration? Default configuration
 Warning: you will not be able to edit these selections.
 How do you want users to be able to sign in? Username
 Do you want to configure advanced settings? No, I am done.
Successfully added auth resource awsamplifyreactapp936d4487 locally

Some next steps:
"amplify push" will build all your local backend resources and provision it in the cloud
"amplify publish" will build all your local backend and frontend resources (if you have hosting category added) and provision it in the cloud

# Deploy the authentication service:

$ amplify push --y
✔ Successfully pulled backend environment staging from the cloud.

Current Environment: staging

| Category | Resource name              | Operation | Provider plugin   |
| -------- | -------------------------- | --------- | ----------------- |
| Auth     | awsamplifyreactapp936d4487 | Create    | awscloudformation |
⠧ Updating resources in the cloud. This may take a few minutes...

UPDATE_IN_PROGRESS amplify-amplifybce972215ef64-staging-25332 AWS::CloudFormation
:::::::::::::::
CREATE_IN_PROGRESS amplify-amplifybce972215ef64-staging-25332-authawsamplifyreactapp936d4487-1WVNCQ30W02SI AWS::CloudFormation
:::::::::::::::
CREATE_COMPLETE    amplify-amplifybce972215ef64-staging-25332-authawsamplifyreactapp936d4487-1WVNCQ30W02SI AWS::CloudFormation
:::::::::::::::
UPDATE_COMPLETE amplify-amplifybce972215ef64-staging-25332 AWS::CloudFormation

```
