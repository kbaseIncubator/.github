## New Repository

**Contents**

- [Create Repository From Template](#create-repository-from-template)
  - [New Repo Demo](#new-repo-demo)
- [Next Steps](#next-steps)
---

### Create Repository From Template

To create a new [github.com/kbase](https://github.com/organizations/kbase/repositories/new) repo and enable the KBase build scripts automatically, simply:

1. Create a new repo in the `kbase` organization.
2. Under the `Repository template` dropdown, select `kbase-template`.
3. Be sure to check the `Include all branches` checkbox.
4. Enter the name of your repo, and set it to `Public` visibility.
5. Click `Create repository`.
6. Once complete, your new repo will include all required branches and workflows.

##### New Repo Demo

<!-- This code creates a simple dropdown -->
<details>
<summary>Expand For Demo</summary>

![NewRepo](https://user-images.githubusercontent.com/6155956/163659879-711f5674-cfda-4d94-8db4-68e9a629dc5f.gif)

</details>

---

### Next Steps

Before using these actions, please:

1. Review the [Development Workflow](development-workflow.md) and [Release Workflow](release-workflow.md) sections.
2. Enable the required [status checks](enable-branch-rules.md#require-status-checks).
3. File a request with the DevOps team (via Jira or Slack) to make any resulting images [public](https://docs.github.com/en/packages/learn-github-packages/configuring-a-packages-access-control-and-visibility#configuring-access-to-container-images-for-an-organization).


---
**|| Previous: [Home](README.md) || Next: [Existing Repository](existing-repository.md) ||**
