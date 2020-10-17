I built this using tutorial from Traversy Media: https://www.youtube.com/watch?v=HRmdj-HpJyE

Key Points:

1. npm init first because you want to set up the db and json-server first before react
2. npx create-react-app client  // this sets up react in a folder called client
3. npm install concurrently
4. Go into the package.json file in the main folder and create the following scripts to start the app:
    "scripts": {
    "server": "json-server --watch db.json --port 5000",
    "start": "npm start --prefix client", //tells it to look in the folder named client to find the start script
    "dev":"concurrently \"npm run server\" \"npm run client\"" //concurrently run both scripts to be able to use the backend and frontend
  },
