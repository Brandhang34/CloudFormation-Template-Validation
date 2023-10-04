# CloudFormation Template checker

## Introduction

These files will be used to check for best practices and security flaws in cloudformation templates you are uploading to AWS CodeCommit. Creating the pipeline will reference the buildspec.yaml file, installing the necessary dependencies and use other checks defined in the .pre-commit-config.yaml file.

### [CFN-Lint](https://github.com/aws-cloudformation/cfn-lint)

Makes sure that the templates are linted and are following best practices

### [CFN-Nag](https://github.com/stelligent/cfn_nag)

Finds for insecure infrastructure that may be defined in the templates.

#### Note

Please make sure to edit the buildspec.yaml file and replace the ```git config``` values.

The templates stored should be in the "templates" directory, as it will prevent any templates to be stored in the main directory. Nested directories shouldn't be an issue if you want to organize further.
