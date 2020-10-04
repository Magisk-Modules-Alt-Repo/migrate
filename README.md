# Migrate
Tools and information for mirroring existing repositories to another repository.

# Usage
`./migrate <USERNAME> <REPONAME> <DESTREPO>`

An organization name can be substituted for the username input field.

Additionally, you must export two environmental variables:

* `GIT_USER`: Your GitHub username
* `GIT_TOKEN`: Your GitHub token / password

These are required to create the repository via the Git API. Ensure your specified user is privileged enough to do this.

# GitHub Action
This repo has a GitHub Action to allow devs to mirror their repositories on-the-fly. This is currently only for moderators with repo access. If you decide to fork this repo, make sure you set the repo secrets AUTH_NAME (GitHub username) and AUTH_KEY (GitHub token / password).
