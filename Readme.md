### Project 1: https://yzhura.github.io/ViteMultipleProjectsDeployment/Project1/dist/index.html

### Project 2: https://yzhura.github.io/ViteMultipleProjectsDeployment/Project2/dist/index.html

# Add new project for deployment:

go to `.github/workflows/deploy.yml`
and add new steps:

```
# New proj:
- name: Build NewProject
  working-directory: ./NewProject
  run: |
    npm install
    npm run build
```

where `NewProject` is the name of your project.
