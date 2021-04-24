This issue collects various links to useful Semgrep resources and documentation in one place so you can reference it if you ever get stuck.

* [semgrep.dev](https://semgrep.dev/) - Semgrep's home page
  * [@returntocorp/semgrep](https://github.com/returntocorp/semgrep) - Semgrep's source code on GitHub
* [Semgrep Registry](https://semgrep.dev/explore) - Home of Semgrep's free, out-of-the-box rules (that is, security checks), written by r2c and the community.
  * These rules are grouped into "rulesets" that collect related functionality, like rules that check for [secrets](https://semgrep.dev/p/secrets), target specific languages (e.g. [javascript](https://semgrep.dev/p/javascript)) or frameworks (e.g. [django](https://semgrep.dev/p/django)), or even entire vulnerability classes (e.g. [xss](https://semgrep.dev/p/xss) or [insecure
    transport](https://semgrep.dev/p/insecure-transport)).
  * [@returntocorp/semgrep-rules](https://github.com/returntocorp/semgrep-rules) - The source code of Semgrep's rules on GitHub.
    * Note that the Registry has more rules than what's just in the `returntocorp/semgrep-rules` repo, as the Registry includes Semgrep rules from other community repos, like NodeJSScan or [Go rules](https://github.com/dgryski/semgrep-go) by [Damian Gryski](https://twitter.com/dgryski).
* [Semgrep Playground](https://semgrep.dev/editor) - Write and share Semgrep rules right from your browser, no installation required!

## Rule Writing

There's a step by step rule writing tutorial [here](https://semgrep.dev/learn).

If you go to the [Playground](https://semgrep.dev/editor), you can also click the "Examples" button to view a number of illustrative built-in examples.

And of course, you can also review the over 1,000 rules in [@returntocorp/semgrep-rules](https://github.com/returntocorp/semgrep-rules).

## Docs

Semgrep has pretty extensive docs, which you can [view here](https://semgrep.dev/docs/).

Of note:
* [Pattern syntax](https://semgrep.dev/docs/writing-rules/pattern-syntax/) - All of the ways you can match code within one pattern.
* [Rule syntax](https://semgrep.dev/docs/writing-rules/rule-syntax/) - All of the ways you can **combine** Semgrep patterns to form more complex queries. For example, looking for code that matches `this` AND `that`, or `this` but NOT `that`, etc.

## Community

Feel free to join the [r2c community Slack](https://r2c.dev/slack) to ask questions (we're super responsive!) or reach out to us on Twitter ([@r2cdev](https://twitter.com/r2cdev)), or send us an email at support@r2c.dev.