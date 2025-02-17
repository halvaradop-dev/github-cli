# Github CLI

This is Github tool based in the terminal. The command used for the operations is `gh`

## Commands

### Repo

Create a repository
```sh
gh repo create

# Options
## Create repository on the web and locally
gh repo create -c

## Add .gitignore template. The first letter of the templates are in uppercase
gh repo create -g Node

## Public Repo
gh repo create --public

## Add README.md file
gh repo create --add-readme

## Description of the repo
gh repo create --description "description message"

## Add License
gh repo create --license "MIT"
```

### Issue

Create an Issue

```sh
gh issue create --repo owner/repo

# Options
## Set the label of the issue
gh issue create --label

## Set the responsible of the issue
gh issue create --assignee "github-user"

## Open the editor to create the issue with this we can add the title and the body
gh issue create -e 

## Define the title of the issue
gh issue create --title "Title"

## Define the body of the issue
gh issue create --body "Body"

## Set the repo to add the issue
gh issue create --repo
```

#### Commentaries
```sh
## Create a new commentary in an issue section and open the text editor
gh issue comment n-issue -e

## Create a new commentary in an issue section with a defined body
gh issue comment n-issue --body

## Update the previous comment
gh issue comment n-issue --edit-last
```

#### List

```sh
## Shows the issues affected by an author
gh issue list --author "Author"

## Shows the issues with a specific state
gh issue list --state {open or closed or all}

## Show the issues with a specific label
gh issue list --label name
```


#### Edit

```sh
# Update the body of an issue
gh issue edit n-issue --body

## Add a label to an issue
gh issue edit n-issue --add-label "Label"

## Assign an issue to an user
gh issue edit n-issue --add-assignee "github-user"
```

#### Close

```sh
gh issue close n-issue --comment "message" --reason|-r "completed | not planned"
```