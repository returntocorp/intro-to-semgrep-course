## Congrats on writing your first rule! 🎉

Holy moly, you:
* Rolled out Semgrep in CI
* Learned how to write custom rules
* **Wrote** a custom rule
* and rolled it out to scan every new PR

...all in a few minutes 🤯

### Automate the Boring Parts of Code Review

> Are there comments you (or developers at your company) often write on PRs?

Wouldn't it be nice if you could *automate* that work and spend your time on higher leveraged things? I think you know where I'm going with this 😉

### Scaling to Thousands of Repos

Oh another thing - did you notice how easy it was to add new rules you write to your scanning policy, with one click from the Playground?

Well imagine you're scanning 100s or 1,000s of repos with Semgrep, and there's something new you'd like to enforce, whether it's a secure guardrail, a new anti-pattern you'd like to block, based on a recent penetration test report or bug bounty submission, etc.

So you quickly write the rule in the Playground, add it to one of your scanning policies, and then *boom*, that rule is **immediately** going to run on every new PR for repos using that policy.

No need to file PRs on hundreds of repos, no need to wait on developers or DevOps teams acting on your request, just quick security coverage, everywhere.

(Note: of course you want to roll out new rules carefully, to ensure they're high signal, don't bother our developer friends, etc.)

## ⌨️ Activity: Write Your First Custom Rule

Time for the next rule writing challenge!

I've opened up a new PR with more code to match: [click here to continue]({{ route_pr_url }}).

<hr>
<h3 align="center">Visit the <a href="{{ route_pr_url }}">next PR</a> to continue.</h3>