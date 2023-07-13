### Migrating single repo ADO to GitHub

```
gh gei migrate-repo --ado-org e2esainstructor \
--ado-team-project <ado-src-project> --ado-repo <ado-src-repo> \
--github-org <github-target-org-name> \
--github-repo <github-target-repo-name>
```
NOTE: <github-target-repo-name> can't be any existing repo name under <github-target-org-name>

### Migrating single repo GitHub to GitHub
```
gh gei migrate-repo --github-source-org <source-org-name> \
--github-target-org <target-org-name> \
--source-repo <source-repo-name> \
--target-repo <target-repo-name> \
--wait
```
