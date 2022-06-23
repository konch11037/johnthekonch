# Starting a server

## Starting boilerplate NUXT 

This is how to start a nuxt application from boilerplate

`npx nuxi init PROJECT_NAME` or `yarn create nuxt-app PROJECT_NAME`

### installing all dependencies

`npm install`

### Starting a server

`yarn dev`

## Starting a manual instilation

1. Make a project directory with the projects name
2. Create `pckage.json` with the following

```
{
  "name": "my-app",
  "scripts": {
    "dev": "nuxt",
    "build": "nuxt build",
    "generate": "nuxt generate",
    "start": "nuxt start"
  }
}
```

3. Then add nuxt with `yarn add nuxt`
