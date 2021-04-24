Great! I've merged in the Semgrep config you set up into this branch so we can iterate on rules and see the results right in this PR.

## Houston, We Have Scan Results

After the check suite finishes, you should see a PR comment warning about the use of `eval()` in the code this PR is adding in [eval_test.ts]({{ url }}).

And check your notifications in the r2c community Slack, you should see a message from the webhook flagging this issue as well.