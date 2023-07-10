### Migrating single repo ADO to GitHub

```
gh gei migrate-repo --ado-org "<ado-source-org-name>" \
--ado-team-project "<ado-source-project-name>" \
--ado-repo "<ado-source-repo-name>" \
--github-org "<target-org-name-in-github>" \
--github-repo "<unique-repo-name-to-be-created-in-github>"
```

### Migrating single repo GitHub to GitHub
```
gh gei migrate-repo --github-source-org <source-org-name> \
--github-target-org <target-org-name> \
--source-repo <source-repo-name> \
--target-repo <target-repo-name> \
--wait
```
