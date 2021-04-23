## Getting Started

Alright, let's do a few quick things to get you up and running. 

### Join the Slack

r2c Community Slack


Many security teams choose 

### Create a Semgrep App Account

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

## ⌨️ Activity: Create a Dashboard Account, Set up Slack Notifications

1. Join the [r2c community Slack](https://r2c.dev/slack) and the appropriate workshop channel.
2. Log in to the [Semgrep Dashboard](https://semgrep.dev/manage/).
3. Set up Slack Notifications.
   1. Go to the [Incoming WebHooks page](https://r2c-community.slack.com/apps/new/A0F7XDUAZ-incoming-webhooks) on the Slack App Directory, and in "Post to Channel" choose your name. This way, all notifications are going to be sent to you via direct message.
   2. Copy the "Webhook URL" generated on the next page (it should look like: `https://hooks.slack.com/services/...`) and go to the [Semgrep Integrations](https://semgrep.dev/manage/integrations) page, create a new integration, select "Slack", provide a name, paste in the webhook url, then save it.
   3. Click the "Test" button, and you should see a message from Semgrep in Slack.

<hr>
<h3 align="center">Comment on this pull request when you're ready and I'll respond with the next step.</h3>


