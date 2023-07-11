## If 'ado-org' is not mentioned then it will consider every org the PAT( Personal Access Token) has access to
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

```
gh gei generate-script --github-source-org e2einstructor --github-target-org adomigration --output migrate_script.sh
```
