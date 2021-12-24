# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

# Building Dashboards Quickly with React and Material-UI

 ## Please install dependency
 - npm install @material-ui/core
 - npm install @material-ui/icons
 - npm install recharts@2.0.0-beta.6
 - npm install fontsource-roboto

## Import font 
import 'fontsource-roboto'; in src/index.js

## clone thema dashboard from github
Now that we have all the modules installed, we’ll need to pull in our example dashboard components. Head over to the Material-UI GitHub and clone this repository into a separate folder (outside of the new dashboard directory):
git clone https://github.com/mui-org/material-ui.git

## copy the component .js
Now we’ll copy the component .js files into our dashboard app directory (we won’t need the TypeScript .tsx files for now):
cp -r material-ui/docs/src/pages/getting-started/templates/dashboard/*.js dashboard/src/

## import Dashboard
Finally, let’s edit our app to use the new components. Head back into the dashboard app directory and open up src/App.js. Near the top of the file, after the last import statement add another import to pull in the new Dashboard component:
import Dashboard from './Dashboard';

## Next, remove everything inside of <div className="App"> and replace it with the following:
<Dashboard />
import './App.css';
import Dashboard from './Dashboard';
function App() {
  return (
    <div className="App">
      <Dashboard />
    </div>
  );
}
export default App;
  
## Last, we need to make one small style tweak so that everything looks correct. Edit the src/Dashboard.js file and change the following line:
theme.palette.mode === 'light'
to
theme.palette.type === 'light'
  
## Great! We should now have all the pieces in place to run our new dashboard app. Go ahead and save the changes and boot up the app:
npm start
  
## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
