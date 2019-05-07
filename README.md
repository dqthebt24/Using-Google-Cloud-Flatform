# Using-Google-Cloud-Flatform to Deploy Nodejs App

## Introduction
This document to show how to deploy a nodejs app using google cloud flatform

## Steps by steps

- Step 1:  Create an app
- Step 2: Download and install Cloud SDK. 

    - To do download and install, following this [link](https://cloud.google.com/sdk/docs/)
    - **Note**: 
    
        - If you already have the Cloud SDK installed, update it by running the following command:
    
            ```gcloud components update```
    
        - To create new configuration. Run this command: 
    
             ```gcloud init```
    
- Step 3: Create new project on cloud

    - Run this code to create: ```gcloud projects create [YOUR_PROJECT_NAME] --set-as-default```
    
    - Verify the project was created: ```gcloud projects describe [YOUR_PROJECT_NAME]```
    
    **The result will look like this**:
    ```
    createTime: year-month-hour
    lifecycleState: ACTIVE
    name: project-name
    parent:
    id: '433637338589'
    type: organization
    projectId: project-name-id
    projectNumber: 499227785679
    ```
- Step 4: Initialize your App Engine app with your project and choose its region:
  
   - Run this code: ```gcloud app create --project=[YOUR_PROJECT_NAME]```
   
   - **Note**: If your project is already exist, you will get an message like this:
   
   > *ERROR: (gcloud.app.create) The project [your-project-name] already contains an App Engine application. You can deploy your application using `gcloud app deploy`.*
   
- Step 5: Deploy 

    - Go to the app directory, create a file name: **app.yaml** with this content
    ```
    # [START gae_quickstart_yaml]
    runtime: nodejs10
    # [END gae_quickstart_yaml]
    ```
    
    - Do deploy by code:```gcloud app deploy```
    
    - Wait the progress will be finished
    
    
## References:
- [Google's document](https://cloud.google.com/nodejs/getting-started/hello-world)

    
