# nodejs-web-app
Creating a Full CI/CD Pipeline on AWS with Jenkins, Slack, and GitHub

# server
`npm i`

`npm run watch`

`goto->browser->type-> http://localhost:8000/`

`goto->browser->type-> http://localhost:8000/users`

`npm run test:unit`

`npm run test:integration`

`npm run test:load`

# tests dockerization

`docker image build -t hello:world -f test.Dockerfile .`

`docker container run -d -i --name testing-ctr hello:world`

`docker container exec -it testing-ctr /bin/sh`

`npm run test:unit`

# prod dockerization

`docker image build -t hello:prod -f prod.Dockerfile .`

`docker container run -d -i --name production-ctr -p 8000:8000 hello:prod`

`goto->browser->type-> http://localhost:8000/`

`docker container exec -it production-ctr /bin/sh`

`npm i loadtest`

`npm run test:load`