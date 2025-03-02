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

## Pull Request

### Create

```sh
## Create a pull requset
gh pr create

## Define the branch ref or target of the pull request
gh pr create --base branch

## Define the branch that create the pull request this value is by default the current branch
gh pr create --head branch

## Create the pull request with the information of the first commit
gh pr create --fill-first

## Define the title of the PR
gh pr create --title "title"

## Define the body of the PR
gh pr create --body "body"

## Add labels to the PR
gh pr create --label

## Open the editor to create the title and body of the PR
gh pr create --edito or -e

## Mark the pull request as draft
gh pr create --draft or -d
```

### Merge

```sh
## Merge the pull request with admin privileges
gh pr merge --admin

## Set Body Text For the Merge Commit
gh pr merge --body "message"

## Options to merge the pull request
gh pr merge --squash or --rebase

## Set Subject Text For the Merge Commit
gh pr merge --subject

## Delete the branch merged locally and remote
gh pr merge --delete-branch
```

### Draft

```sh
## Make a pull request as a draft
gh pr ready n-pr --undo

## Make a pull request ready for review (disabled draft)
gh pr ready n-pr
```

### Comment

```sh
## Add a body for the comment
gh pr comment n-pr --body or -b

## Edit the last comment
gh pr comment n-pr --edit-last

## Open the default editor to add the body to the comment
gh pr comment n-pr --edito or -e
```

### Close

```sh
## Message to the closed pull request
gh pr close n-pr --comment or -c "message" 

## Delete the branch of the pull request after to be closed
gh pr close n-pr --delete-branch or -d
```