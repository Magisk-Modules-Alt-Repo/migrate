# mmar-migrate
Tools and information for mirroring existing repositories to the Alt-Repo.

# Usage
Use the following command to mirror a specified repository to the Magisk-Modules-Alt-Repo as a [Mirror] repo, and automatically add a GitHub workflow to update it every 30 minutes.

`./migrate <USERNAME> <REPONAME>`

An organization name can be substituted for the username input field.

Additionally, you must export two environmental variables:

* `GIT_USER`: Your GitHub username
* `GIT_TOKEN`: Your GitHub token / password

These are required to create the repository via the Git API. Ensure your specified user is privileged enough to do this.

# GitHub Action
This repo has a GitHub Action to allow devs to mirror their repositories on-the-fly. **DO NOT USE THIS HERE**. Your personal access token or password will be saved in the Action log. It is much, *much* saver to fork this repository to your own private account and use it there.
