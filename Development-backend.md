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
