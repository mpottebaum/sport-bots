# Sport Bots

## Installing Sport Bots

To install Sport Bots, follow these steps:

1. Clone the full contents of this repo and its submodules

```
git clone --recurse-submodules git@github.com:mpottebaum/sport-bots.git
```

2. Install gems in the back end directory:

```
cd sport-bots-api
bundle
```

3. Still in the back end directory, build the database:

```
rails db:create
rails db:migrate
rails db:seed
```

4. Install dependencies in the front end directory:

```
cd sport-bots-frontend
npm install
```

## Using Sport Bots

To use Sport Bots, follow these steps:

1. From the sport-bots-api directory, start the API server:

```
rails s
```

2. From the sport-bots-frontend directory, start the front end server.

```
npm start
```

The front end server will run on `localhost:3001`. If you need to use a different port, run the following command (instead of `npm start`) with the port number of your choice where it says `3001`:

```
PORT=3001 node server
```