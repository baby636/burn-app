# burn-app
An automated Bitcoin Cash wallet that forwards payments on to the token-liquidity app with an OP_RETURN instruction to burn tokens.




This repository is a boilerplate for building APIs with
[koa2](https://github.com/koajs/koa/tree/v2.x) and Mongo DB.
This repository was originally forked from Adrian Obelmejias'
[koa-api-boilerplate repository](https://github.com/adrianObel/koa2-api-boilerplate).
It makes the following modifications:

- Removes babel as a dependency. This repository is now naively compatible with
  node v8.9 or higher.

- Replaced `bcrypt` dependency with `bcryptjs`. This improves compatibility across
  versions of node.js and across OSs.

- Configured for Jenkins (continuous integration), Coveralls (code coverage), Green Keeper (automated dependency management), and Semantic Release (automated versioning).

- 'Production' environment is targeted for packaging as a Docker container.

- 'admin' user type added in addition to standard 'user' type. Allows the creation
of private vs public APIs that only be accessed by an admin. Useful for privileged
commands like updating and deleting other users.

 - Winston logging integrated for daily rotated logs and a maximum size of
 1 megabyte.

 - Linting enforced with [Husky](https://github.com/typicode/husky) and [JavaScript Standard Style rules](https://www.npmjs.com/package/standard).

## Features
This project covers basic necessities of most APIs.
* Authentication (passport & jwt)
* Database (mongoose)
* Testing (mocha)
* Doc generation with apidoc
* Linting using standard
* Packaged as a Docker container



## Requirements
* node __^10.15.1__
* npm __^6.7.0__

## Installation
```bash
git clone https://github.com/christroutner/koa-api-boilerplate
cd koa-api-boilerplate
npm install
npm start
```

## Structure
```
├── bin
│   └── server.js            # Bootstrapping and entry point
├── config                   # Server configuration settings
│   ├── env                  # Environment specific config
│   │   ├── common.js
│   │   ├── development.js
│   │   ├── production.js
│   │   └── test.js
│   ├── index.js             # Config entrypoint - exports config according to envionrment and commons
│   └── passport.js          # Passportjs config of strategies
|
├── production               # Dockerfile for build production container
|
├── src                      # Source code
│   ├── lib                  # Business logic libraries
│   ├── modules
│   │   ├── controller.js    # Module-specific controllers
│   │   └── router.js        # Router definitions for module
│   ├── models               # Mongoose models
│   └── middleware           # Custom middleware
│       └── validators       # Validation middleware
└── test                     # Unit tests
```

## Usage
* `npm start` Start server on live mode
* `npm run dev` Start server on dev mode with nodemon
* `npm run docs` Generate API documentation
* `npm test` Run mocha tests
* `docker-compose build` Build a 'production' Docker container
* `docker-compose up` Run the docker container

## Documentation
API documentation is written inline and generated by [apidoc](http://apidocjs.com/).

Visit `http://localhost:5000/docs/` to view docs


## Dependencies
* [koa2](https://github.com/koajs/koa/tree/v2.x)
* [koa-router](https://github.com/alexmingoia/koa-router)
* [koa-bodyparser](https://github.com/koajs/bodyparser)
* [koa-generic-session](https://github.com/koajs/generic-session)
* [koa-logger](https://github.com/koajs/logger)
* [MongoDB](http://mongodb.org/)
* [Mongoose](http://mongoosejs.com/)
* [Passport](http://passportjs.org/)
* [Nodemon](http://nodemon.io/)
* [Mocha](https://mochajs.org/)
* [apidoc](http://apidocjs.com/)
* [ESLint](http://eslint.org/)

## IPFS
v2.3.0 uploaded to IPFS:

- Get it: `ipfs get QmUz4b2KwNLNvHZRTYcgrPCuKAhMB73XWN8vY8LLVVEYV1`
- Pin it: `ipfs pin add -r QmUz4b2KwNLNvHZRTYcgrPCuKAhMB73XWN8vY8LLVVEYV1`

## License
MIT

test
