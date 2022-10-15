

## KBase Build & Release Guide

This guide describes how to set up and use the standard KBase build and release workflows.


<img width="937" alt="KBaseActions" src="https://user-images.githubusercontent.com/6155956/195962864-b560614d-a908-406a-bf48-64b8135d7016.png">

The reusable workflows discussed in this guide allow KBase developers to:

- Automatically build test images when a pull request is created
- Tag images as `latest` once a pull request is merged
- Create production-ready images with semantic versions (e.g. `1.1.4`) using GitHub's [Release](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases) process
- Enable repos to use optional fully automated [continuous deployment](https://en.wikipedia.org/wiki/Continuous_deployment) to development (e.g. `CI`) enviroments once these environments are deployed on Rancher2.

---

### Contents

#### Enable Build Workflows

  - [New Repository](./guide/new-repository.md)
  - [Existing Repository](./guide/existing-repository.md)

#### Enable Required Branch Rules

- [Enable `development` and `main`/`master` branch rules](./guide/enable-branch-rules.md)

#### 	Workflow Processes

- [Development Workflow](./guide/development-workflow.md)
- [Release Workflow](./guide/release-workflow.md)


---
**|| Next: [New Repository](./guide/new-repository.md) ||**

