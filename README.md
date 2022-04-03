# Docker Worflow 

Deploy a React app using GitHub, Travis CI, and AWS. 

### Project Structure 
Node version: 
```Shell 
v14.18.1
```

Project created with: 
```shell
npx create-react-app frontend
```

### Run 
```shell
# Start the dev server
npm run start 

# Run tests 
npm run test

# Build a production version of the app
npm run build
```

### Docker 

#### Dockerfile
Build the image and run the container: 
```shell
# Build image 
docker build -f Dockerfile.dev -t docker-workflow/react .

# Run the container 
docker run -p 3000:3000 docker-workflow/react
```
Real-time update using volumes
```shell
docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app docker-workflow/react
```

#### Docker Compose
