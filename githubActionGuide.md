# GitHub Action Guide

## OutLine
- Descriptions
- Basic Concepts

## Description: 
An event automatically triggers the workflow, which contains a job. The job then uses steps to control
the order in which actions are run. These actions are the commands that automate your software testing.

## Baic Concepts

### Workflows:
The workflow is an automated procedures that you add to your repository. Workflows are made of one or more jobs 
and can be scheduled or triggered by an event. The workflow can be used to build, test, package, or deploy a project
on GitHub.

### Events:
An event is a specific activity that triggers a workflow. For example, activity can originate from GitHub when someone
pushes a commit to a repository or pull request is created. You can also use the repository dispatch webhooks to trigger
a workflow when an external event occurs.

### Jobs:
A job is a set of steps that executes on the same runner. By default, a workflow with multiple jobs in parallel.
You can also configure a workflow to run jobs sequentially. For example, a workflow can have two sequential jobs 
that builds and test the code, Where the test job is dependent on the status of the build job. If the build job fails,
the test job will not run.

### Steps: 
A step is an individual task that can run commands in a job. A step can be either an action or a shell command.
Each step in a job executes on the same runner, allowing the actions in the job to share data with each other.

### Actions:
Actions are standalone commands that are combined into steps to create a job.
Actions are the smallest portable building block of of a workflow. You can create your own actions, or use
actions created by the GitHub community. To use an action in a workflow, you must include it as a step.

### Runners:
A runner is a server that has the GitHub Actions runner application installed. You can use runners hosted by GitHub, 
or you can host your own.A runner listens for available jobs, runs one job at the time, and report the progress logs,
 and results back to GitHub. For GitHub-hosted runners, each job in a workflow runs in a fresh virtual environment.
