

# Lazydeploy

## Installation

On Ubuntu/Linux:

* Download this repository, using git or directly from github page (in that case you will need to unzip it too);
* Open the terminal an place yourself in the directory where it is downloaded;
* Be sure you got `root` permissions in the terminal;
* run `chmod +x ./lazydeploy`
* run `cp lazydeploy /bin/lazydeploy`

## Configuration

In the same path of the application you want to deploy, create a file called LAZYNESS with this content: 

```bash
LAZY_S3_BUCKET="artifact001"
LAZY_PATH="artifacts/"
LAZY_CODEDEPLOYROLE="CodeDeployRole-123456789"
LAZY_EXCLUDE="--exclude=.env --exclude=*node_modules* --exclude=*dist*"
LAZY_APP="appname"
```

> Take care to do **NOT** use the same `LAZY_APP` name of you production env when deploying in stage.

S3 bucket should already exist, the same as the path and the CodeDeploy role. 

`LAZY_EXCLUDE` will exclude files or folders from being zipped and deployed. 

## Usage

```bash
lazydeploy <EC2_INSTANCE_NAME>
```

Example:
```bash
lazydeploy hakuna-503
```