# Game-of-Bands-Express 
An API Backend for the Gameofbands website.


## Description:
Full CRUD for the Gameofbands song database, with required Reddit Authentication. 

## Technologies
- Express.js
- Node.js
- Various Oauth 2.0 Abstraction libraries
- Redis Session Store
- Redis Server


## Installation
1. Clone down the repository and `cd` into it
    
    ```
    git clone github.com/daniel-edminster/Game-of-Bands-Express && cd Game-of-Bands-Express
    ```
    
    Setup your MongoDB with atlas or a local installation and run `node db/seed.js`


2. Install dependencies

    Note: This is not deployable to Heroku without $$ due to the Redis Dependency. This inconvenience also forces the use of `pm2` to run the API server as a background process instead of 'the Heroku way'
    ```
    npm install
    sudo npm install -g pm2
    sudo apt-get install redis-server redis-cli
    
    ```

3. Initialize API
    Note: You will need to provide your own SSL cert or code around my implementation to initialize this locally. See `certbot` by letsencrypt to get started with that. Additionally, you will need to modify the CORS headers to match the URI of whatever front-end you tie to this.

    ```
    redis-server &
    pm2 index.js
    ```



## Usage
See `/docs/` folder of this repository for a list of all available routes. There are a lot of read routes. For a batch display the only ones really used are `/all/desc` and `/song/:id`



## Contribute

- Source: https://github.com/daniel-edminster/Game-of-Bands-Express
- Issue Tracker: https://github.com/daniel-edminster/Game-of-Bands-Express/issues


