# LAB-03: Build Artifact Workflow

## Goal

Your goal is to see the application packaged as a build artifact.

## Why This Lab Matters

In the CI lab, we verified the code.

In this lab, we go one step further:

We package the application and keep the packaged output.

For this lab, you do not need to build Docker locally on your laptop.

GitHub Actions will do the build work for you.

## File for This Lab

Open this file in your repository:

`.github/workflows/03-build-artifact.yml`

## Step 1: Read the Workflow File

Read the file once before running it.

You should be able to find:

- the test step
- the Docker build step
- the artifact upload step

## Step 2: Run the Workflow Manually

Open the `Actions` tab.

Open `03 Build Artifact Workflow`.

Use `Run workflow` to start the workflow manually.

## Step 3: Open the Workflow Run

Open the new run and watch the steps.

You should see steps like:

- `Check out repository`
- `Set up Python`
- `Run tests`
- `Build Docker image`
- `Save Docker image as artifact file`
- `Upload build artifact`

## Step 4: Find the Artifact

On the workflow run page, look for the artifact section.

You should see an artifact named:

`tiny-health-app-image`

You do not need to inspect the file contents for this lab.

The important point is that the workflow produced a packaged output and saved it.

## Step 5: Explain the Story in Your Own Words

Try to describe the workflow like this:

1. the workflow checks the app
2. the workflow packages the app
3. the workflow saves the package for later use

## What You Should Notice

This workflow is important because it creates a reusable output.

That output can be used later in deployment instead of rebuilding from scratch again.

## If the Workflow Fails

Check these things first:

1. open the failed step
2. see whether the failure happened in tests or in the Docker build
3. read the first clear error message
4. compare your files with the course example

If the Docker step fails, ask your instructor for help before changing many lines.

## Success Check

You are done when:

- the workflow passes
- you can see the artifact name on the run page
- you can explain the difference between code and artifact

## Reflection

After the lab, try to answer these questions:

- Why is a build artifact useful?
- Why is an image different from a container?
- Why is saving the packaged output better than relying only on source code?
