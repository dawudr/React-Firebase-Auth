This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

# Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

# Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm ci && npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify

## Firebase Hosting
Learn more: 
[https://firebase.google.com/docs/cli#install_the_firebase_cli](https://firebase.google.com/docs/cli#install_the_firebase_cli)

[https://medium.com/swlh/how-to-deploy-a-react-app-with-firebase-hosting-98063c5bf425]([https://medium.com/swlh/how-to-deploy-a-react-app-with-firebase-hosting-98063c5bf425])

### `npm install -g firebase-tools`
Update to the latest CLI version

### `firebase login`
Login with your credentials.

### `firebase projects:list`
The displayed list should be the same as the Firebase projects listed in the Firebase console.

If you’re wondering, env-cmd library is a simple node program for executing commands using an environment from an env file.

### `npm i -D env-cmd`

Now, I will create aliases for both projects by running:

### `firebase use --add`
Link to firebase project created in console.

### `firebase init hosting`
Initialize your project

```
? What do you want to use as your public directory? build
? Configure as a single-page app (rewrite all urls to /index.html)? Yes
? Set up automatic builds and deploys with GitHub? No
? File build/index.html already exists. Overwrite? No
'
```


### `firebase deploy --only hosting`
Deploy to your site


## Set up the GitHub Action to deploy to Firebase Hosting
Learn more:

[https://firebase.google.com/docs/hosting/github-integration](https://firebase.google.com/docs/hosting/github-integration)

[https://medium.com/firebase-developers/the-comprehensive-guide-to-github-actions-and-firebase-hosting-818502d86c31](https://medium.com/firebase-developers/the-comprehensive-guide-to-github-actions-and-firebase-hosting-818502d86c31)


The first thing we need to do is authorize with GitHub
The Firebase CLI OAuth app asks to be authorized on your behalf so we can do two things: upload a secret to GitHub’s secret store and check to see if you own the repo you’re setting up a workflow with. That’s it.
The CLI creates a Service Account on your behalf and uploads its secret keys to GitHub’s secret store.
The CLI looks to write a file in the workflow folder called firebase-hosting-pull-request.yml. If you want to deploy to live on a merge to your main branch you’ll also have a file called firebase-hosting-merge.yml

`firebase init hosting:github`

dawudr/React-Firebase-Auth
In GitHub, create a new branch and commit the workflow yaml files created by the CLI. Merge the branch.


`firebase hosting:channel:deploy`
Preview and share
