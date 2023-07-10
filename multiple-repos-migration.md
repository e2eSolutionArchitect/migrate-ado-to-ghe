
## Generate script for bulk migration
```
gh gei generate-script --github-org <github-target-org-name> \
--ado-org <ado-source-org-name> \
--output migrate_script.sh \
--repos-only
```

- The above 'repos-only' will only consider migration for repositories. 
- The above command will generate migrate_script.sh as output file. If using PowerShell rename it to '.ps1' e.g, migrate_script.ps1 
- Now just simply run this migrate_script.sh in the terminal or command line interface (CLI). It will migrate every repo to the target org in GitHub.
- If 'ado-org' is not mentioned then it will consider every org the PAT( Personal Access Token) has access to
- Similarly, if 'repos-only' is not mentioned then it will consider every team project and repos the PAT( Personal Access Token) has access to

```
gh gei generate-script --github-org <github-target-org-name> \
--output migrate_script.sh 
```

### Run the script
```
./migrate_script.sh
```
