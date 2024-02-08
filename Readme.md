### Project 1: https://yzhura.github.io/ViteMultipleProjectsDeployment/Project1/dist/index.html

### Project 2: https://yzhura.github.io/ViteMultipleProjectsDeployment/Project2/dist/index.html

# Add new project for deployment:

go to `.github/workflows/deploy.yml`
and add new steps:

```sh
# New proj:
- name: Build NewProject
  working-directory: ./NewProject
  run: |
    npm install
    npm run build
    rm -rf node_modules
```

where `NewProject` is the name of your project.

and for all new projects change `vite.config.js`

```js
  base:
    process.env.NODE_ENV === 'development'
      ? '/'
      : '/YourRepoName/Project1/dist',
```

where `YourRepoName` is the name of your repository
and `Project1` is the name of your project (name of folder)
