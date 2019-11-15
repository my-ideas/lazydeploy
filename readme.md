# USAGE 

```bash
./lazydeploy ec2 <EC2_INSTANCE_NAME> <S3_BUCKET> <S3_PATH> <CODEDEPLOYROLE> [--exclude ]
```

Example:
```bash
lazydeploy ec2 hakuna-503 pipeline app/ CodeDeployRole "--exclude=*git* --exclude=.env --exclude=*node_modules* --exclude=*dist*"
```