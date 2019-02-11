# tfe_variables_aws

### Purpose of the repsoitory
- Example on how to use variables in TFE UI to create EC2 instance in AWS.

### List of files files in respository.
- main.tf - file with terraform configuration code.

### How to use this repository
- Install `terraform` by following this [instructions](https://www.terraform.io/intro/getting-started/install.html).
- Assuming you have TFE account you need to create new workspace and link it to this repo.
- Next you need to declare variables in the workspace you just created and assign values to those variables
- For variables `access_key` and `secret_key` use sensitive option, for the rest you can leave as default.
- Also make sure your variables in TFE workspace are defined in your `main.tf` code and the names are the same. 
- Clone the repository to your local computer: `git clone git@github.com:nikcbg/tfe_variables_aws`.
- Go into the cloned repo on your computer: `cd tfe_variables_aws`.
- Next commit some changes to your GitHub by creating a pull request.
- Next merge the pull request, after merging:
  - this will trigger a plan run in TFE which you can watch in TFE workspace that is link to this repo unders runs
  - if no issues you can apply the changes by clicking the apply button under the plan window.
  - you can watch the apply command executing.
  - after it is done you can check your AWS console to see the EC2 instance created.

### How to destroy resources from TFE UI
- To destroy the EC2 instance you just created in AWS, you need to do the followinf:
   - declare environment varible in your workspace that you linked to this repo.
   - environment varibles are located under Terraform Variables in the workspace.
   - the name of the variable has to be `CONFIRM_DESTROY` and the value set to `1`.
 - Next go to `Settings` and choose `Destruction and Delition` on the bottom of the drop-down menu.
 - Next click on `Queueing a destroy Plan ` and you can watch how the infrastructure it's been destroyed.
 
 
 
