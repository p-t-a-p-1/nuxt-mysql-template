# Docker + Nuxt.js(Vue.js + Express.js) + MySQL

Building a Nuxt.js and MySQL environment with Docker

Technologies:
* Docker(Docker-compose)
* Nuxt.js(Vue.js + Express.js)
* MySQL:5.7

## Getting Started

### Launch the Nuxt sample application and run it.

1. Please clone this repository to your local environment.

```bash
$ git clone git@github.com:p-t-a-p-1/nuxt-mysql-template.git
```

2. Use docker-compose to build the service and start the container.

```bash
$ docker-compose up -d --build
```

3. Enter the nuxt container with the `exec` command.

```bash
$ docker-compose exec nuxt /bin/sh
```

4. In the container, install `create-nuxt-app` with the version specified.

```bash
/usr/src # npm install -g create-nuxt-app@2.15.0
```

5. Create a nuxt application using the `create-nuxt-app` command.

```bash
/usr/src # npx create-nuxt-app test-app
```

6. After answering a few questions, a Nuxt application will be created.

```bash
create-nuxt-app v2.15.0
✨  Generating Nuxt.js project in test-app
? Project name test-app
? Project description My stunning Nuxt.js project
? Author name 
? Choose programming language JavaScript
? Choose the package manager Npm
? Choose UI framework None
? Choose custom server framework Express
? Choose Nuxt.js modules Axios
? Choose linting tools Prettier
? Choose test framework None
? Choose rendering mode Universal (SSR)
? Choose development tools jsconfig.json (Recommended for VS Code)

...
...
...


🎉  Successfully created project test-app

  To get started:

        cd test-app
        npm run dev

  To build & start for production:

        cd test-app
        npm run build
        npm run start

```

7. Edit nuxt.confid.js to unify the port and host information between the docker and the local server.

```nuxt.confid.js
module.exports = {
  mode: 'universal',
  // ポートとホストの設定
  server: {
    port: 3000,
    host: '0.0.0.0',
  },
  
...
...
...

```

8. Launch the application with the `npm run dev` command. Then, you will see the following screen on http://localhost:3000.

```bash
/usr/src # cd test-app/
/usr/src/test-app # npm run dev
```

![スクリーンショット 2020-09-07 22 26 06](https://user-images.githubusercontent.com/51960141/92396268-b93a1500-f15f-11ea-879d-e0d636e4f5d3.png)

