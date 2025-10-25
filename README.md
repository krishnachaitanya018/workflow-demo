Create a custom action workflow where one workflow calls another workflow to perform the pipeline.

Understanding why you built this entire workflow: 

I created a modular CI/CD pipeline in GitHub Actions where one workflow triggers another using workflow_call.
This structure promotes reusability and cleaner automation — similar to how enterprise teams separate trigger pipelines and build pipelines.
It automatically runs a Python program, validates outputs, and demonstrates how CI/CD can be version-controlled with the code.”

What You Built:
We are building two connected GitHub Actions workflows —
where one workflow (main-caller.yml) triggers or “calls”
another workflow (build-runner.yml) to perform some task (like building or running a program).

Main explanation:
When you push code or update the Python file,
GitHub triggers main-caller.yml,
which calls build-runner.yml,
which then runs your updated Python code.

build-runner.yml = the worker that performs the job
main-caller.yml = the controller that tells the worker when to start
