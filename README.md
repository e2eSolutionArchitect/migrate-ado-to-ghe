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
- Generate Personal Access Token (PAT) from source and target repositories. GitHub > Settings > Profile > Personal Access Token
- Set the privileges appropriately while creating the token. check required access [here](https://docs.github.com/en/migrations/using-github-enterprise-importer/preparing-to-migrate-with-github-enterprise-importer/managing-access-for-github-enterprise-importer#required-roles-for-github)
- set environment variables 'GH_SOURCE_PAT' (source PAT), 'GH_PAT' (target PAT)
- These two variables can be passed with 'gh gei ' command but the best practice is to set as environment as a secure approach

## Tips
- check the available commands for gh gei by running 'gh gei --help' or 'gh gei migrate-repo --help'

### Install GH extension
#### Run the below commands in GitHub CLI
```
# Check the installed extension list
gh extension list
```
#### The extension for GEI (GitHub Enterprise Importer) is located [here](https://github.com/github/gh-gei)
Please check the installation instruction for the extension [here](https://github.com/github/gh-gei#readme)

```
# To install gei
gh extension install github/gh-gei

# verify installation
gh extension list
```


### To be tested

### Migrating single repo
```
gh gei migrate-repo --ghes-api-url https://<api url> \
--github-source-org <source-org-name> \
--github-target-org <target-org-name> \
--source-repo <source-repo-name> \
--target-repo <target-repo-name> \
--wait
```

Note: 
- There is a size limit over which importer doesn't work. migration file size > (it may change over time)
