Great! Now we're going to set up Semgrep scanning every PR via GitHub actions by creating a `semgrep.yml`.

Though we're going to be using GitHub Actions in this workshop, because Semgrep is nice and portable, easily runnable as a standalone binary or Docker, it's pretty easy to set up Semgrep in pretty much any CI platform under the sun.

See [these docs](https://semgrep.dev/docs/sample-ci-configs/) for info about setting up Semgrep in GitLab, Buildkit, CircleCI, or other providers, and [see here](https://semgrep.dev/docs/semgrep-ci/#semgrep-ci) for more info about Semgrep in CI.

## ⌨️ Activity: Set up Semgrep in CI

1. On the [Projects page](https://semgrep.dev/manage/projects), select the "Add CI job to GitHub project" option, and click the "Get started" button.
   1. Semgrep's GitHub App is going to ask for a few, minimal permissions so it can auto-set things up for you (create a PR adding `semgrep.yml` to repos you want to onboard, etc.).
   2. If you want, you can only add the Semgrep GitHub App to this `intro-to-semgrep` repo. If you want to add more repos, you select "All repositories" or hand select a few more. You can always update this later via your GitHub profile [Installed Applications settings](https://github.com/settings/installations).
2. After you've authorized the Semgrep GitHub App, navigate back to the [Projects page](https://semgrep.dev/manage/projects), click the "Refresh projects from GitHub button", and then click the "Add CI job" button next to the `intro-to-semgrep` repo row.
3. On the next page, click the "Commit file" button, then follow the instructions for setting up a GitHub Secret on the `intro-to-semgrep` repo.
   1. Note that we're adding the Secret to just this repo. If you want to run Semgrep across many of your or your org's repos, you probably want to add this Secret at your profile or org level, so you don't have to add it one repo at a time.
4. A Semgrep scan will automatically start. We'll examine the results later, for now, comment on this PR and let's get writing some rules!


<hr>
<h3 align="center">Comment on this Pull Request once you've finished onboarding Semgrep (`semgrep.yml` GitHub Actionn) to this repo.</h3>