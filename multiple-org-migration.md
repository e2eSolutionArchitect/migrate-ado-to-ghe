[check here](https://github.com/github/gh-gei#azure-devops-to-github-usage)

## For ADO to GHE

```
gh ado2gh generate-script --ado-org ORGNAME --github-org ORGNAME --all
gh ado2gh generate-script --ado-org e2einstructor --github-org adomigration --all
```

```
### Github to Github
gh gei generate-script --github-source-org ORGNAME --github-target-org ORGNAME

### ADO to Github
gh ado2gh generate-script --ado-org ORGNAME --github-org ORGNAME --all
```

### If 'ado-org' is not mentioned then it will consider every org the PAT( Personal Access Token) has access to
```
gh ado2gh generate-script  --github-org ORGNAME --all

gh gei generate-script --github-org <github-target-org-name> --output migrate_script.sh
```

## For single org migration specify target org

```
gh ado2gh generate-script --ado-org <ado-source-org-name> --github-org ORGNAME --all
gh gei generate-script --github-org <github-target-org-name>  --github-target-org <github-source-org-name> --output migrate_script.sh 
```


