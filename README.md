* I have used ExpressJS for this project

### Installing dependencies

* From within project's root folder run `npm install` and it will install all the dependencies available in the package.json file.

### Running the app

* From within project's root folder run `npm start` or `node index.js` and it will init an already existent blockchain. At present, I've configured it to add a new block everytime we run the project.
* Or create a new blockchain by deleting the "Blockchain" folder and running `node index.js` in root folder.
* Then navigate to the HTTP server on port 8000

### HTTP endpoints

#### Create Block
```
curl -X POST \
  http://localhost:8000/block \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'body=teste!'
```

#### Get block by height
```
curl -X GET \
  http://localhost:8000/block/0
```

#### Get chain length
```
curl -X GET \
  http://localhost:8000/chainLength
```

#### Get the whole chain
```
curl -X GET \
  http://localhost:8000/chain
```
