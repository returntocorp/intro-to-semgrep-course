## Getting Started

Alright, first we'll do a few quick things to get you up and running.

At a high level, here's what we're going to do:

**Join the r2c Community Slack** - There's a channel for this workshop you can ask questions in, and we'll use it to set up notifications when Semgrep finds issues.

**Create a free Semgrep App account** - This lets us easily manage Semgrep in CI, set up notifications, configure scanning policy, view results over time, and more.

## ⌨️ Activity: Create a Dashboard Account, Set up Slack Notifications

1. Join a Slack channel that allows you to add webhook notifications, or create a new Slack instance if you don't have one available.
2. Log in to the [Semgrep Dashboard](https://semgrep.dev/manage/).
3. Set up Slack Notifications.
   1. Visit the Slack App Directory (`https://your_slacks_name.slack.com/apps`), search "Incoming WebHooks", and in "Post to Channel" choose your name. This way, all notifications are going to be sent to you via direct message.
   2. Copy the "Webhook URL" generated on the next page (it should look like: `https://hooks.slack.com/services/...`) and go to the [Semgrep Integrations](https://semgrep.dev/manage/integrations) page (you may need to click on "Integrations" in the left hand side navbar), create a new integration, select "Slack", provide a name, paste in the webhook url, then save it.
   3. Click the "Test" button, and you should see a message from Semgrep in Slack.
   4. See the [Slack integration docs](https://semgrep.dev/docs/notifications/#slack) for additional details.
4. Now, on the [Semgrep Policies page](https://semgrep.dev/manage/policies), click on each policy, go to Settings -> Integrations -> Add, select the Slack notification you set up, and click "Save".


Feel free to join the [r2c community Slack](https://r2c.dev/slack) and ask questions in `#general` or `#workshop-2021-owasp-devslop` if anything is unclear.

<hr>
<h3 align="center">Comment on this pull request when you're ready and I'll respond with the next step.</h3>


