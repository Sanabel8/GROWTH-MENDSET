## Introduction to Amazon S3
* Simple Storage Service (S3)
* Amazon Simple Storage Service (Amazon S3) is storage for the Internet. It is designed to make web-scale computing easier.
* Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web.
### Advantages of using Amazon S3
1. Creating buckets 
2. Storing data 
3. Downloading data
4. Permissions
5. Standard interfaces
### Amazon S3 concepts
Topics: 
1. Buckets
2. Objects
3. Keys
4. Regions
5. Amazon S3 data consistency model

* Buckets serve several purposes:
1. They organize the Amazon S3 namespace at the highest level.
2. They identify the account responsible for storage and data transfer charges.
3. They play a role in access control.
4. They serve as the unit of aggregation for usage reporting.

## S3 with Amplify
### Getting started
* The Amplify Storage category provides an interface for managing user content for your app in public, protected, or private storage buckets.
* The Amplify CLI helps you to create and configure the storage buckets for your app. 
### Provision backend storage
1. amplify add storage
2. Enter the following: 
? Please select from one of the below mentioned services:
    `Content (Images, audio, video, etc.)`
? You need to add auth (Amazon Cognito) to your project in order to add storage for user files. Do you want to add auth now?
    `Yes`
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
? Please provide a friendly name for your resource that will be used to label this category in the project:
    `S3friendlyName`
? Please provide bucket name:
    `storagebucketname`
? Who should have access:
    `Auth and guest users`
? What kind of access do you want for Authenticated users?
    `create/update, read, delete`
? What kind of access do you want for Guest users?
    `create/update, read, delete`
? Do you want to add a Lambda Trigger for your S3 Bucket?
    `No`
3. amplify push
4. added to build.gradle (Module: app):  
 implementation 'com.amplifyframework:aws-storage-s3:1.24.0'
 implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
5. make  Sync Now.
6. added :
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.addPlugin(new AWSS3StoragePlugin());



































