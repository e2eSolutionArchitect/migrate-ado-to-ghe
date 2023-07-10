
## Generate script for bulk migration
```
gh gei generate-script --github-org <github-target-org-name> \
--ado-org <ado-source-org-name> \
--output migrate_script.sh \
--repos-only
```

The above 'repos-only' will only consider migration for repositories. 
The above command will generate migrate_script.sh as output file. If using PowerShell rename it to ps1. 
Now just simply run this migrate_script.sh in the terminal or command line interface (CLI). It will migrate every repo to target org in github.

```
./migrate_script.sh
```
