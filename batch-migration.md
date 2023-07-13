## Generate script for bulk migration
```
### Github to Github
gh gei generate-script --github-source-org <github-source-org-name> \
--github-target-org <github-target-org-name> \
--all --output migrate.sh

### ADO to Github
gh ado2gh generate-script --ado-org <ado-source-org-name> \
--github-org <github-target-org-name> \
--all --output migrate.sh
```

- The above 'repos-only' will only consider migration for repositories. 
- The above command will generate migrate.sh as output file. If using PowerShell then rename the file to '.ps1' e.g, migrate_script.ps1 
- Now simply run this migrate_script.sh in the terminal or command line interface (CLI). It will migrate every repo to the target org in GitHub.
- If 'ado-org' is not mentioned then it will consider every org the PAT( Personal Access Token) has access to
- Similarly, if 'repos-only' is not mentioned then it will consider every team project and repos the PAT( Personal Access Token) has access to

```
gh gei generate-script --github-org <github-target-org-name> \
--output migrate.sh 
```

### Run the script
```
./migrate.sh
```



## WAIT
Have you received the below warning while generating the migration script?
**[WARNING] CANNOT FIND GITHUB APP SERVICE CONNECTION IN ADO ORGANIZATION: e2esainstructor. You must install the Pipelines app in GitHub and connect it to any Team Project in this ADO Org first.**

### If 'github-org' or 'ado-org' is not mentioned then it will consider every org the PAT( Personal Access Token) has access to
```
gh ado2gh generate-script  --github-org <github-target-org-name> --all --output migrate.sh

gh gei generate-script --github-source-org <github-target-org-name> --all --output migrate.sh
```

## For single org migration specify target org

```
gh ado2gh generate-script --ado-org <ado-source-org-name> --github-org <github-target-org-name> --all --output migrate.sh
gh gei generate-script --github-source-org <github-source-org-name>  --github-target-org <github-target-org-name> --output migrate_script.sh 
```


Good read [check here](https://github.com/github/gh-gei#azure-devops-to-github-usage)
