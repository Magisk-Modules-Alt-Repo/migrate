# mmar-migrate
Tools and information for mirroring existing repositories to the Alt-Repo.

# Usage
Use the following command to mirror a specified repository to the Magisk-Modules-Alt-Repo as a [Mirror] repo, and automatically add a GitHub workflow to update it every 30 minutes.

`./migrate -m <USERNAME> <REPONAME>`

An organization name can be substituted for the username input field.

Additionally, you must export two environmental variables:

* `GIT_USER`: Your GitHub username
* `GIT_TOKEN`: Your GitHub token / password

These are required to create the repository via the Git API. Ensure your specified user is privileged enough to do this.

If you want to clone a repo without bundling the 30m automatic update workflow, omit the `-m` flag. This will simply migrate the repo. This option is ideal for approving `[Module]` submissions.

# GitHub Action
This repo has a GitHub Action to allow devs to mirror their repositories on-the-fly. This is currently only for moderators with repo access. If you decide to fork this repo, make sure you set the repo secrets AUTH_NAME (GitHub username) and AUTH_KEY (GitHub token / password).
