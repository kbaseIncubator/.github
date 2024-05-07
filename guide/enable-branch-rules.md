## Enable Required Branch Rules

**Contents**

- [Assumptions](#assupmtions)
- [Preliminary Steps](#preliminary-steps)
- [Enable Branch Rules](#enable-branch-rules)
   -  [Develop Branch Rules](#develop-branch-rules)
   -  [Main Branch Rules](#main--master-branch-rules)
   - [Branch Rules Demo](#branch-rules-demo)
- [Next Steps](#next-steps)
---

### Assumptions

The KBase Actions (workflows) are built under the assumption that:

- All work is performed in feature branches (with names matching JIRA or GitHub issue numbers)
- Feature branches are merged via pull requests to the `develop` branch
- Pre-release code is merged to `main`/`master` via a pull request
- Semantic relesases are created with the [GitHub Release](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository) process
- The branch rules below are enabled on the repo to prevent build failures

### Preliminary Steps

1. Confirm that  `pr_build.yml` and `release-main.yml` exist in the `.github/workflows/` directories of all active branches.
2. See [New Repository](new-repository.md) and [Existing Repository](existing-repository.md) for instructions on how to enable these workflows.

### Enable Branch Rules

To prevent failed build checks, two branch rules _must_ be enabled on the new repo.

The following steps will allow a repo owner/admin to set up the needed protection rules:

| ⚠️ These steps can only be performed by a repository owner or admin. |
| :----------------------------------------------------------: |



#### Develop Branch Rules

1. Navigate to the `Settings` tab in the repository.
2. Click the `Branches` option on the left link under `Code and automation`.
3. Verify that the default branch is set to `develop`.
4. Under `Branch protection rules`, click `Add rule`.
5. Under `Branch name pattern`, enter `develop`.
6. Check the following boxes under `Protect matching branches`:
   - Require a pull request before merging
   - Require approvals (1 approver is fine)
   - Require status checks to pass before merging
   - Require branches to be up to date before merging
7. Click Create.

#### Main / Master Branch Rules

1. Repeat steps 1-6 above, setting the `Branch name pattern` to `main`.
2. In addition, check the `Include administrators` checkbox.
   - This can be safely disabled by an admin during troublehooting, but should remain enabled during normal use.
3. Click create.

#### Require status checks

Once a successful Pull Request has been created, and the `pr_build.yml` workflow has completed, require the following specific status checks:

- On `develop` branch rule: `build-develop-open / build-image`
- On `main` branch rule: `build-main-open / build-push-image`

<img width="1298" alt="RequiredStatusChcecks" src="https://user-images.githubusercontent.com/6155956/195523313-350f9a34-5e64-440f-8dcc-ed4e1186f315.png">

##### Branch Rules Demo

<!-- This code creates a simple dropdown -->
<details>
<summary>Expand For Demo</summary>

![BranchRulesDemo](https://user-images.githubusercontent.com/6155956/164119527-330c67cc-4ad6-423a-9e92-2d5a042526e9.gif)

</details>

---

### Next Steps

Before using these branch rules, please:
1. Review the [Development Workflow](development-workflow.md) and [Release Workflow](release-workflow.md)
2. File a request with the DevOps team (via Jira or Slack) to make any resulting images [public](https://docs.github.com/en/packages/learn-github-packages/configuring-a-packages-access-control-and-visibility#configuring-access-to-container-images-for-an-organization).


---
**|| Previous: [Existing Repository](existing-repository.md) || [Home](README.md) || Next: [Development Workflow](development-workflow.md) ||**
