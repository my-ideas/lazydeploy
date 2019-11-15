# USAGE 

```bash
./lazydeploy ec2 <EC2_INSTANCE_NAME> <S3_BUCKET> <S3_PATH> <CODEDEPLOYROLE> [--exclude ]
```

Example:
```bash
lazydeploy ec2  beekube-prod-worker-gracious-hoover-503 bk-pipeline-global-artifact001 artifacts/global/dockerkan/ beekube-users-CodeDeployRole-1H7HJYH9IW87E "--exclude=*git* --exclude=.env --exclude=*node_modules* --exclude=*dist*"
```