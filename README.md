# JIRA <3 GitHub

We can now use the [JIRA DVCS Connector](https://marketplace.atlassian.com/plugins/com.atlassian.jira.plugins.jira-bitbucket-connector-plugin) plugin to reference our commits on GitHub from JIRA issues

## How to do it

Just put the JIRA issue number in your commit message, and once it is pushed to GitHub then JIRA will add a link to that commit from the JIRA issue page. Remember to include the complete relevant project code and issue number e.g. MBG-8296, COM-568

[A commit with a JIRA issue number in the commit message]

[Developer box on JIRA issue]

[JIRA issue Commits list with the above commit]

## Feature branches and pull requests

JIRA will also include feature branches and pull requests if any commit within them contains the JIRA issue number - it won't check the name of the branch or PR.

[Developer box with branches and pull requests]

[A JIRA issue branches list]

[A JIRA issue pull requests list]

## Making comments from your commit messages

Include #comment in your commit message to automatically make a matching comment on the JIRA issue page

[Commit message with #comment in it]

[JIRA issue comment from the above commit]

## FAQks

### What repositories and JIRA projects can I use this on?

All GitHub repositories under the CRUKorg organisation, and all projects in CRUK JIRA.

### I pushed my commit to GitHub but it didn't hasn't appeared on the JIRA issue page

Do not worry, it can take up to 60 minutes for JIRA to update with the latest commits from GitHub.

### My commit appeared in the JIRA issue, but it isn't attributed to my JIRA account
### OR: I made a #comment in my commit message, but it never came through on the JIRA issue page

Check that you are creating your git commits with your JIRA account's email address. Run this command from inside the git repository to see your configured git email address:

```
git config user.email
```

If it does not match the email address in your [JIRA profile](https://jira.cancerresearchuk.org/secure/ViewProfile.jspa), update it like this:

```
git config user.email david.collard@cancer.org.uk
```

Or update it globally for all your repositories like this:

```
git config --global user.email david.collard@cancer.org.uk
```

## External links

* [Use the JIRA DVCS Connector Add-on](https://confluence.atlassian.com/display/BITBUCKET/Use+the+JIRA+DVCS+Connector+Add-on) - Atlassian documentation on the JIRA DVCS Connector with more of what is now possible from commit messages
* [DVCS Accounts](https://jira.cancerresearchuk.org/secure/admin/ConfigureDvcsOrganizations!default.jspa) - JIRA plugin administration page
