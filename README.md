# Cloud-Photo-Album-Storage Application

## Live Demo
[https://d16rk8ket78in4.cloudfront.net](https://d16rk8ket78in4.cloudfront.net) 

### Front-End
    React JS
### Back-End
    AWS - serverless
### API
    GraphQL

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

## Build instructions
After checking out this code, you'll need to run the following commands to get this app to work.
**In your terminal, from within the same directory as this README, perform these steps:**

### 1. Initialize Amplify
Run: `amplify init`

Answer the questions like this:
- Choose your default editor: `<anything you want>`
- Choose the type of app that you're building `javascript
- Please tell us about your project
- What javascript framework are you using `react`
- Source Directory Path:  `src`
- Distribution Directory Path: `build`
- Build Command:  `npm run-script build`
- Start Command: `npm run-script start`
- Do you want to use an AWS profile? `<either answer is fine, it's up to you>`

Wait for `amplify init` to finish

### 2. Add authentication
Run: `amplify auth add`

Answer the questions like this:
-  Do you want to use the default authentication and security configuration? `Yes, use the default configuration.`

Run `amplify push`, Press `Enter/Return` to continue, and wait for it to finish

### 3. Add a GraphQL API
Run: `amplify api add`

Answer the questions like this:
- Please select from one of the below mentioned services `GraphQL`
- Provide API name: `<whatever you want -- I suggest 'photoAlbumsDemo'>`
- Choose an authorization type for the API `Amazon Cognito User Pool`
- Do you have an annotated GraphQL schema? `Yes`
- Provide your schema file path: `scripts/bootstrapping/schema.graphql`

Run `amplify push`, Press `Enter/Return` to continue, and wait for it to finish

### 4. Add S3 file storage
Run: `amplify storage add`

Answer the questions like this:
- Please select from one of the below mentioned services `Content (Images, audio, video, etc.)`
- Please provide a friendly name for your resource that will be used to label this category in the project: `photostorage`
- Please provide bucket name: `<accept the default value>`
- Who should have access: `Auth users only`
- What kind of access do you want for Authenticated users `read/write`

Run `amplify push`, Press `Enter/Return` to continue, and wait for it to finish

### 5. Publish the app to the CloudFront CDN
Run `amplify hosting add`

Answer the questions like this:
- Select the environment setup: `PROD (S3 with CloudFront using HTTPS)`
- hosting bucket name `<accept the default>`
- index doc for the website `index.html`
- error doc for the website `index.html`

Run `amplify push`, Press `Enter/Return` to continue, and wait for it to finish

Run `amplify publish` and wait for it to finish