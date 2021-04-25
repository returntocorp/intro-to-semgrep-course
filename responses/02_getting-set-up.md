## Getting Started

Alright, first we'll do a few quick things to get you up and running.

At a high level, here's what we're going to do:

**Join the r2c Community Slack** - There's a channel for this workshop you can ask questions in, and we'll use it to set up notifications when Semgrep finds issues.

**Create a free Semgrep App account** - This lets us easily manage Semgrep in CI, set up notifications, configure scanning policy, view results over time, and more.

## ⌨️ Activity: Create a Dashboard Account, Set up Slack Notifications

1. Join the [r2c community Slack](https://r2c.dev/slack) and the `#workshop-2021-owasp-devslop` channel.
2. Log in to the [Semgrep Dashboard](https://semgrep.dev/manage/).
3. Set up Slack Notifications.
   1. Go to the [Incoming WebHooks page](https://r2c-community.slack.com/apps/new/A0F7XDUAZ-incoming-webhooks) on the Slack App Directory, and in "Post to Channel" choose your name. This way, all notifications are going to be sent to you via direct message.
   2. Copy the "Webhook URL" generated on the next page (it should look like: `https://hooks.slack.com/services/...`) and go to the [Semgrep Integrations](https://semgrep.dev/manage/integrations) page (you may need to click on "Integrations" in the left hand side navbar), create a new integration, select "Slack", provide a name, paste in the webhook url, then save it.
   3. Click the "Test" button, and you should see a message from Semgrep in Slack.
4. Now, on the [Semgrep Policies page](https://semgrep.dev/manage/policies), click on each policy, go to Settings -> Integrations -> Add, select the Slack notification you set up, and click "Save".

<hr>
<h3 align="center">Comment on this pull request when you're ready and I'll respond with the next step.</h3>


