Including hard-coded secrets in source code is dangerous, as the source code may leak, be compromised, or be pushed to a public location on GitHub.

There have been a number of cases where leaked AWS, GitHub, or other API keys have lead to companies being compromised, having user data leaked, huge cloud bills run up, and more.

Let's try to prevent that from happening in the first place.

## ⌨️ Activity: Finding Secrets

The [Semgrep Registry](https://semgrep.dev/explore) comes with over 1,000 rules from r2c and the community that provide out-of-the-box coverage for a variety of vulnerability classes, including the Top 10.

Here we're going to leverage the Registry to quickly start scanning for secrets.

(*Note: at the time of this writing, the Secrets pack is included in Semgrep Cloud's default policies. This means that the first step is unnecessary. I've left those instructions in as examples of how to add rulesets to your scanning Policies.*)

1. Visit the [Secrets ruleset page](https://semgrep.dev/p/secrets), click the "Add to Policy" button to add it to your "Security Policy" policy, and [re-scan this PR]({{ secrets_checks_page_url }}).
2. Review the [files changed]({{ files_changed_url }}) in this PR (you can also click on the "Files changed" tab at the top of this page), and note that it looks like there are some API tokens that are not currently being flagged by Semgrep's built-in secret detection rules.
    *  Let's create a rule to detect these secrets! We can see that they appear to start with `CUSTOMAPI_` and end with 10 digits.
    * We can copy the structure of one of the existing secrets rules. I've done that for you [here](https://semgrep.dev/s/clintgibler:learning-lab-custom-api-secret).
    * Add a regex that matches both cases. Hint: use [regex101](https://regex101.com/) if you need help.
3. When you're done, click the "Add to Policy" button to add it to your "Security Policy" policy, and [re-scan this PR]({{ checks_page_url }}).

<hr>
<h3 align="center">Yay, you're done!</h3>
