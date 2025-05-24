Video 2 notes
npx -> package manager
npx create-react-app(utility) 01basicreact

How to understand react packages/projects->
-package.json(main entry point) under src
-consists of project name, dependencies, testing libraries, scripts.
-web-vitals condemns the performance of the app(record/tracking performance)
-scripts run the project or prepares the project for production
under scripts: 
start, build, test, eject
start: runs the project in development environment
build: final product of the app on browser(compiled version) 
test: for running the test cases 
eject: for ejecting react itself till a certain progression

npm run start (for starting the project)
npm run build(for building the project-> creates a build folder which contains static assests like html css and compiles the entire react code into js files)

creating a project with vite
->npm create vite@latest
will ask the project name and what tech to build the project on
->project folder will be ready
->npm install to install the dependencies
->npm run dev to run the project 