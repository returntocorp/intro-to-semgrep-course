Great! Now we're going to set up Semgrep scanning every PR via GitHub actions by creating a `semgrep.yml`.

Though we're going to be using GitHub Actions in this workshop, because Semgrep is nice and portable, easily runnable as a standalone binary or Docker, it's pretty easy to set up Semgrep in pretty much any CI platform under the sun.

See [these docs](https://semgrep.dev/docs/sample-ci-configs/) for info about setting up Semgrep in GitLab, Buildkit, CircleCI, or other providers, and [see here](https://semgrep.dev/docs/semgrep-ci/#semgrep-ci) for more info about Semgrep in CI.

## ⌨️ Activity: Set up Semgrep in CI

1. Set up Semgrep's API token.
   1. Within the Dashboard, go to the [Settings page](https://semgrep.dev/manage/settings) and create a new Semgrep token.
   2. Navigate to this repo's [Secrets page]({{ secrets_setting_url }}), create a new repository secret named `SEMGREP_APP_TOKEN`, and copy in the token value from the prior step.
2. Configure `semgrep.yml` to point to your Dashboard account.
  1. On the Dashboard [Settings page](https://semgrep.dev/manage/settings), copy the value of `publishDeployment` into [`semgrep.yml` in this repo]({{ url }}).
<hr>
<h3 align="center">I'll respond in this pull request when I detect a comment posted to it.</h3>