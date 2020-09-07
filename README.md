# nuxt-mysql-template

# usage

```bash

$ git clone git@github.com:p-t-a-p-1/nuxt-mysql-template.git

$ docker-compose up -d --build

$ docker-compose exec nuxt /bin/sh

/usr/src # npm install -g create-nuxt-app@2.15.0

/usr/src # npx create-nuxt-app test-app

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


```bash
/usr/src # cd test-app/
```


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


```bash
/usr/src/test-app # npm run dev
```

![スクリーンショット 2020-09-07 22 26 06](https://user-images.githubusercontent.com/51960141/92396268-b93a1500-f15f-11ea-879d-e0d636e4f5d3.png)

