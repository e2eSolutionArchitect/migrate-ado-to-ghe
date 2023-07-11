[check here](https://github.com/github/gh-gei#azure-devops-to-github-usage)

## For ADO to GHE

```
gh ado2gh generate-script --ado-org ORGNAME --github-org ORGNAME --all
gh ado2gh generate-script --ado-org e2einstructor --github-org adomigration --all
```


## For Github to Github

### If 'ado-org' is not mentioned then it will consider every org the PAT( Personal Access Token) has access to
```
gh gei generate-script --github-org <github-target-org-name> \
--output migrate_script.sh
```

## For single org migration just mention ado-org

```
gh gei generate-script --github-org <github-target-org-name> \
--ado-org <ado-source-org-name> \
--output migrate_script.sh 
```


