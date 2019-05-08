made using https://medium.com/@deanvniekerk/simple-net-core-webpack-and-react-overview-using-vs-code-5522da657b35

dotnet new web -o alchemylab


Steps:
1) Add MVC service  
    - MVC = model view controller: its a type of framework https://www.tutorialspoint.com/mvc_framework/mvc_framework_introduction.htm
2) Add Controller for Home page (controllers/homecontroller.cs)
3) Add source index
4) Bundle with webpack by adding package.json and running  npm install webpack webpack-cli
5) link bundle.js to index.cshtml
NOTE: We use webpack to work with older browsers like E11

ADD ES6 FEATURES AND BABEL
7) Lets update message.js with template literals
NOTE: If you change a source js file you need to rerun webpack with npm run build
- Babel will adapt template literals to older browsers
    npm install "babel-loader@^8.0.0-beta.3" @babel/core @babel/preset-env -D
8) Install babel, then update webpack.config.js to include it
 - due to this step, we can now use any new ES6 feature and still support older browsers & our js libraries will be packaged into one js file, improving client side performance

 Hotmodules auto update
We currently must rerun webpack and refresh browser to do things: lets get hotmodules to do this for us
after doing this, you start the server using the debug window









## TODO:
- Create additional React components
- Hooking into the React lifecycle events
- Bundle.js minification
- Production vs Development Webpack config files
- Moving all styles to a common css file
- React testing
- Adding Redux for React state management