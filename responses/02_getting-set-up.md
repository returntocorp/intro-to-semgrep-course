## Getting Started

### Installing Semgrep

This isn't a required step, but it might be nice to have Semgrep installed locally so you can easily run scans via CLI.

TODO link to docs, have brew, pip, Docker instructions

### Slack

r2c Community Slack


Many security teams choose 

### Create Semgrep App Account

We need this for managing Semgrep in CI and choosing which rules to run, where.

Totally free for open *and* closed source repos.

Background stuff

#### Set up Slack Notification

Copy in Slack webhook URL provided by r2c into notifications. Configure policy to use those notifications.

#### Add Semgrep Token to GitHub Secrets

Grab token

Add to project Secrets tab

TODO GIF showing the process or Youtube video

We'll walk through the app later.

## ⌨️ Activity: Join Slack, Create Dashboard Account and Semgrep Token

1. Join the [r2c community Slack](https://r2c.dev/slack) and the appropriate workshop channel.
2. Log in to the [Semgrep Dashboard](https://semgrep.dev/manage/).
3. Within the Dashboard, go to the [Settings page](https://semgrep.dev/manage/settings) and create a new Semgrep token.
4. Navigate to this repo's [Secrets page]({{ secrets_setting_url }}), create a new repository secret named `SEMGREP_APP_TOKEN`, and copy in the token value from the prior step.

<hr>
<h3 align="center">I'll respond in this pull request when I detect a comment posted to it.</h3>


