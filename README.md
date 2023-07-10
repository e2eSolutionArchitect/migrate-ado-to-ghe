# Migrate Azure DevOps to Github Enterprise
## Objectives:
- Migrate a single repository from Azure DevOps to Github Enterprise (GHE)
- Migrate multiple repositories in batch from Azure DevOps to Github Enterprise (GHE)
- Migrate ADO 'organization(s)', which contains multiple projects, repos, branches, tags, commits, code review comments,  and pipelines, to GitHub Enterprise (GHE)
-----------------

# Preparation:
- Download Github CLI [click here](https://cli.github.com/)
- Check GitHub CLI installation instructions [click here](https://github.com/cli/cli#readme)
- Install GitHub Enterprise Importer (GEI) extension

### Install GH extension
#### Run below commands in GitHub CLI
```
# Check the installed extension list
gh extension list
```

### To be tested
```
gh gei migrate-repo --ghes-api-url https://<api url> \
--github-source-org <source-org-name> \
--github-target-org <target-org-name> \
--source-repo <source-repo-name> \
--target-repo <target-repo-name> \
--wait
```
