# [nomadcoders.co] Uber Eats Clone [ENG, 2020]

<br/>

## 01. Backend

<br/>

### 004. Backend Setup

    $ yarn global add @nestjs/cli

<br/>

    $ cd app
    $ nest new backend
    $ cd backend
    $ npm run start

<br/>

http://localhost:3000/

<br/>

### 006. Apollo Server Setup

https://docs.nestjs.com/graphql/quick-start

    $ npm i @nestjs/graphql graphql-tools graphql apollo-server-express

<br/>

### 007. Our First Resolver

https://docs.nestjs.com/graphql/quick-start#code-first

<br/>

    $ nest generate module restaurants

<br/>

http://localhost:3000/graphql

<br/>

![Application](/img/pic-part01-les007-pic01.png?raw=true)

<br/>

### 008. ObjectType

<br/>

### 009. Arguments

<br/>

### 010. InputTypes and ArgumentTypes

<br/>

### 011. Validating ArgsTypes

    $ yarn install class-validator class-transformer

<br/>

### 012. TypeORM and PostgreSQL

    $ docker-compose up -d

<br/>

### 015. TypeORM Setup

https://docs.nestjs.com/techniques/database

    $ yarn install @nestjs/typeorm typeorm pg

<br/>

### 016. Introducing ConfigService

    $ yarn install @nestjs/config
    $ yarn install cross-env

<br/>

### 017. Configuring ConfigService

<br/>

### 018. Validating ConfigService

    $ yarn install joi

<br/>
### 019. Our First Entity

<br/>

Run pgadmin in docker container:

```
$ docker run -e PGADMIN_DEFAULT_EMAIL='postgres@test.com' -e PGADMIN_DEFAULT_PASSWORD='password1234' -p 5555:80 --name pgadmin dpage/pgadmin4
```

<br/>

http://localhost:5555/

```
login: postgres@test.com
pass: password1234
```

<br/>

Try to connect to local "host ip" - not localhost

<br/>

### 020. Data Mapper vs Active Record

<br/>

### 021. Injecting The Repository

<br/>

http://localhost:3000/graphql

<br/>

```
{
    restaurants {
        id
    }
}
```

<br/>

![Application](/img/pic-part01-les021-pic01.png?raw=true)

<br/>

### 022. Recap

<br/>

### 023. Create Restaurant

<br/>

### 024. Mapped Types

<br/>

### 025. Optional Types and Columns

<br/>

```
// CREATE RESTAURANT
mutation {
  createRestaurant(input: {
    name: "Nico N",
    isVegan: false,
    address: "nico address"
  })
}
```

<br/>

**returns:**

```
{
  "data": {
    "createRestaurant": true
  }
}
```

<br/>

### 026-027. Update Restaurant

<br/>

```
// UPDATE RESTAURANT
mutation {
  updateRestaurant(input: {
    id: 2,
    data: {
      name: "Nico K",
    isVegan: true,
    address: "nico address upd"
    }

  })
}
```

<br/>

```
{
    restaurants {
        id,
      name,
      isVegan
      address
    }
}
```

<br/>

### 028. User Module Introduction

<br/>

### 029. User Model

    $ nest generate module users
    $ nest generate module common

<br/>

### 030. User Resolver and Service

<br/>

### 031-033. Create Account Mutation

```
// CREATE ACCOUNT OWNER
mutation {
  createAccount(input: {
    email: "owner@gmail.com",
    password: "pass1234"
    role:Owner
  }){
    ok
    error
  }
}
```

<br/>

**returns:**

```
{
  "data": {
    "createAccount": {
      "ok": true,
      "error": null
    }
  }
}
```

<br/>

### 034. An Alternative Error

<br/>

### 035. Hashing Passwords

    $ yarn install bcrypt
    $ yarn install --save-dev @types/bcrypt

<br/>

### 036-037. Log In

```
// LOGIN
mutation {
  login(input: {
    email: "owner@gmail.com",
    password: "pass1234"
  }){
    ok
    error
    token
  }
}
