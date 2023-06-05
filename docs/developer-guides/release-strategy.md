## Branching Strategy

Feature branch workflow is a popular strategy used in software development to manage code changes and collaboration among team members. It involves creating separate branches for each new feature or task being worked on, allowing developers to work on their changes independently without affecting the main codebase. Here's an overview of the feature branch workflow strategy:

#### Branch Creation
When a new feature or task needs to be implemented, a developer creates a new branch from the main development branch (often called the "master" or "main" branch). This new branch will be dedicated to that specific feature.

#### Independent Development
Developers can work on their assigned features in isolation within their respective branches. They can make changes, write new code, and perform tests without affecting the main branch or other developers' work.

#### Regular Commits
As work progresses, developers make regular commits to their feature branches. Commits are used to save changes to the local branch and create a history of the development process. It is good practice to make small, focused commits with clear commit messages.

#### Collaboration and Review
Once a developer completes the implementation of a feature, they can push their branch to a remote repository (such as Git) and create a pull request (PR) or merge request (MR). This allows other team members to review the code changes and provide feedback or suggestions. Code reviews are important for maintaining code quality and catching errors or potential issues before merging into the main branch.

#### Testing and Integration
After the code changes have been reviewed and approved, the feature branch is merged into the main branch. Before merging, it is recommended to run tests on the feature branch to ensure that the new code works correctly and does not introduce any regressions. Once merged, the new feature becomes part of the main codebase.

#### Branch Cleanup
After merging the feature branch, it can be deleted to keep the repository clean and avoid confusion. However, some teams may choose to keep feature branches for reference or to track specific changes. The feature branch workflow allows for parallel development, easier collaboration, and better isolation of changes. It provides a controlled environment for development and reduces the risk of conflicts and issues when multiple developers are working on different features simultaneously.

## GitHub Actions
GitHub Actions are a feature provided by GitHub that allows you to define and automate custom workflows for your software development projects. Workflows are written in YAML format and reside within your repository's .github/workflows directory. They provide a way to define a set of steps or actions that are executed in response to specific events, such as code pushes, pull requests, or scheduled intervals.

Here are some key aspects and concepts related to GitHub Workflows:

Workflow file: A workflow file is a YAML file that defines the workflow. It contains a set of jobs and the associated steps or actions to be executed. You can have multiple workflow files in your repository, each with its own configuration.

Events: Workflows can be triggered by various events, such as push events (when code is pushed to a branch), pull request events (when a pull request is opened or updated), or scheduled events (at specific intervals). You can configure your workflows to respond to specific events.

Jobs: A job represents a unit of work within a workflow. Each job consists of a set of steps or actions to be executed. Jobs can run in parallel or sequentially, depending on your workflow requirements.

Steps: Steps are individual units of work within a job. Each step typically represents a specific action to be performed, such as checking out code, running tests, or deploying an application. You can use pre-defined actions provided by GitHub or create your own custom actions.

Actions: Actions are reusable units of code that can be used in workflows. Actions can be created by yourself, your organization, or the community. They allow you to encapsulate and share common tasks, making workflows more modular and easier to maintain.

Workflow syntax: GitHub Workflows use YAML syntax to define the structure and configuration of your workflows. YAML is a human-readable data serialization format. In workflow files, you define jobs, steps, actions, and their respective configurations using YAML syntax.

Workflow runs and logs: When a workflow is triggered, it creates a workflow run. Workflow runs provide information about the execution of your workflows, including the status, duration, and logs of each step and action. You can view workflow runs in the GitHub Actions tab of your repository.

GitHub Workflows offer powerful automation capabilities, allowing you to automate various aspects of your software development lifecycle, such as building, testing, and deploying applications. They can help streamline your development process, increase productivity, and improve code quality.

#### build-on-pull-request.yml
This workflow triggers on each pull request taised in develop and master branch and runs build for respective module.
#### sast-and-package.yml
This workflow triggers on each pull request taised in develop and master branch and runs CodeQL which is SAST tool and generates war file for respective module.



