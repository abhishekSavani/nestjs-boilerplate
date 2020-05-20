<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

## NestJS With Postgresql

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Installation

- install nestjs CLI globally.

```bash
$ npm i -g @nestjs/cli
```

```bash

$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

# Commands

- create nest module: nest g module module_name
- create controller: nest g controller controller_name --no-spec
- create service: nest g service controller_name --no-spec

- Update Nest dependancy (nest version 6 To nest version 7) :
  nest update -f -t latest

# Notes

when create new module

- create module.
- create controller.
- create service.

- create entity: one kind of database model.
- create repository : for write complex business logic and use in service.

# Packages

class-validator :

- its use in validate DTO.
- DTO is just typescript class is use for define structure of Body, req, res .. etc.
- in simple term you can use it for validate class.

@nestjs/jwt :

- nest js wrapper for JWT.

@nestjs/passport:

- nest js wrapper for passport middlewere.

passport:

- actual passport library.
- manage auth strategy.

passport-jwt:

- manage jwt auth strategy through passport.

win-node-env:

- manage configuration.
- for window: for set node env.

# DB Relationship

one to many | both side
many to one | both side

- note: in this case write relation code in both entity model.

---

## example

User model | task model [65]

- UM have one-to-many relation with TM.
- OneToMany().
- one user have many task
- when we access User that time we need Task for appropriate User.
- this case we make { eager: true }

- TM have many-to-one relation with UM.
- ManyToOne().
- many task have one user.
- many task have one user.
- when we access Task that time if we don't need User for appropriate Tasl.
- this case we make { eager: false }

## Notes

- for more info. check -> notes.txt
- for postman collection -> docs/NEST.postman_collection.json

## Credit

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

Nest is [MIT licensed](LICENSE).
