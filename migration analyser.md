## Analyze migration
Use the [migration analyzer tool](https://github.com/github/gh-migration-analyzer) to estimate and plan for the migration. 

```
# Create a directory 
mkdir ado-to-ghe

# Clone migration analyzer
git clone https://github.com/github/gh-migration-analyzer.git

# Install NPM in the new directory
cd ado-to-ghe
npm install

# Fetch ADO repository
node src/index.js ADO-org -o <ado-org-name>

--------------- 
node src/index.js ADO-org [options]

Options:
  -p, --project <project name> Azure DevOps project name (can pass either project or organization, not necessary to pass both)
  -o, --organization <organization> Azure DevOps organization name
  -t, --token <PAT> Azure DevOps personal access token
  -h, --help Help command for Azure DevOps options

# Check output csv
Output file 'Pull-Requests.csv' under directory named '<ado-org-name>-Pull-Requests'
```
Project	Repository Name	Number Of Pull Requests
e2eSA-demo	e2eSA-demo	0
migrate-ado-ghe	migrate-ado-ghe	0
![image](https://github.com/e2eSolutionArchitect/migrate-ado-to-ghe/assets/8308302/58eee02b-d553-482e-9bdd-48ccb0ebc4bc)
