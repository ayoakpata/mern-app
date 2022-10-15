git clone /
cd client / 
npm install / 
npm start / 
access frontend app via http://localhost:3000/ /

cd server
npm install
npm run app
access backend app via http://localhost:4001/

#build
docker build -f Dockerfile.dev -t metarock/multiclient .

#run & bind port ip to host machine
docker run -it -p 4002:3000 metarock/multiclient

#build
docker build -f Dockerfile.dev -t metarock/multiserver .

#run & bind port ip to host machine
docker run -it -p 4003:5000 metarock/multiserver

#build with docker compose
docker compose up --build

#push
docker push metarock/multiclient

#push
docker push metarock/multiserver
