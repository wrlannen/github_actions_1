# GitHub Actions Challenges

## Challenge 1: Enhance the Build Workflow
Build upon the existing GitHub Actions workflow for your Java project by caching Maven dependencies to improve build performance. Ensure that the cache is configured correctly and that it speeds up the build process.

## Challenge 2: Add Testing and Retain Test Reports
Extend the build workflow to ensure that unit tests are executed and their results are retained. Although Maven runs the tests as part of the build, you need to:
   - Verify that the workflow reports test results correctly.
   - Retain the test reports as artifacts so they are available for review later.

## Challenge 3: Implement Deployment Workflow
Create a separate GitHub Actions workflow for deployment. This workflow should be triggered on pushes to the `main` branch. Instead of deploying to an external environment, ensure that the built artifact (e.g., a JAR file) remains available persists after the build process.

## Challenge 4: Trigger Workflows Sequentially
Configure the build workflow to trigger the deployment workflow upon successful completion. Use the `workflow_run` event to chain the workflows, ensuring that deployment only occurs if the build and tests succeed.

## Challenge 5: Set Up Scheduled Maintenance Workflow
Add a workflow that runs on a schedule, such as daily or weekly, to perform maintenance tasks like cleaning up old artifacts or running health checks. Ensure that this workflow runs independently of other workflows and meets your specified schedule.

## Challenge 6: Manual Trigger Workflow
Create a workflow that can be manually triggered using the `workflow_dispatch` event. This workflow should perform a specific task that you define, such as generating a report or performing additional testing, and can be run on demand via the GitHub Actions UI or API.