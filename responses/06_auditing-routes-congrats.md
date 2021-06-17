Congrats, you'll now get visibility into any time new routes are added to this app without auth!

As a busy security engineer or developer, you probably don't have time to manually audit *every* newly added route, but you *do* have time to audit routes that are potentially risky.

This exercise showed how to quickly flag potentially dangerous code being added, that's **unique to how your code is written.**

No static analysis tool will have rules like this out of the box, as the tool creators have never seen your code nor do they know how it works.

But with Semgrep and a little hackery, we can easily create high signal, high ROI rules, tailored to our environment 🤘

## ⌨️ Next: Finding Secrets

In the next challenge, we'll see how to start scanning every PR for leaked secrets using out-of-the box rules, and write a new rule to find a custom secret type.

Let's go!

<hr>
<h3 align="center">Visit the <a href="{{ route_pr_url }}">next PR</a> to continue.</h3>