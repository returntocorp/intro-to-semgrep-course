## Watching but Not Breaking the Build

Sometimes there are code changes you want to know about, but they're not strictly a bug or vulnerability; that is, you don't want to break the build if they occur.

For example, when you see code:
* Using a sensitive `is_admin()` function
* Performing potentially dangerous functionality, like parsing XML, doing crypto, etc.
* Adding a new route

Semgrep policies make it easy to have fine-grained control over how you want scan results to be handled:
* If you want results only over Slack, email, or other integrations (don't inform developers when matches are founnd)
* If you want PR comments (notify developers, but don't block the build)
* Fail the build (for critical issues you have high confidence in)

Rolling out in notify only mode is a great way to test new rules, to build your confidence in them before rolling them out in PR commenting or blocking mode.

## Intermediate Rule Writing

Here's a few quick tips, but again, see the Issue for links to the full docs.

### Compose Patterns via "or is" (`pattern-either`)

Want your rule to match multiple things? Click the `+` and select `"or is"` one or more times.

These patterns will be considered like a boolean OR - if any match, the Semgrep rule as a whole will match. ([docs](https://semgrep.dev/docs/writing-rules/rule-syntax/#pattern-either))

### Metavariables in messages

When a metavariable (e.g. `$X`) you use in a pattern matches a piece of target code, you can reuse that metavariable in the `message` field.

This way you a can give developers (or you) a more useful, actionable, contextual message, by referencing, for example, the function names or variables involved and why there's an issue.

### Filter Matches via "and is not" (`pattern-not`)

Like "or is" (`pattern-either`), you can combine multiple `pattern-not` clauses to filter out multiple sets of code patterns you *don't* want to match ([docs](https://semgrep.dev/docs/writing-rules/rule-syntax/#pattern-not)).

One common way to approach rule writing is to:
* Write a series of `pattern` or `pattern-either` clauses that match a broad set of code snippets you're interested in.
* Iteratively add `pattern-not` clauses to filter out common "false positives," that is, code you *don't* want to match.

## ⌨️ Activity: Auditing Routes

We're going to start simple, matching just a few routes, and then we'll iteratively improve our rule to make it more precise.

Your rule will largely be the same each time (with some improvements). The reason I'm providing different links in each is because I've changed the comment annotations to make it clear which lines you should and shouldn't be matching.

1. Update [this rule]({{ route_get_playground_url }}) to only match GET routes (`app.get()`).
2. Update [this rule]({{ route_all_playground_url }}) to now match all PUT, POST, and DELETE routes as well.
3. Update [this rule]({{ route_use_playground_url }}) to also include `app.use`, but only when the first argument is a string literal (the path). Include the matched path for any route, regardless of HTTP verb, in the return message.
4. Update [this rule]({{ route_unauth_playground_url }}) to be the above, but only include routes that don't do *any* auth, that is, don't call `security.denyAll()`, `security.isAuthorized()`, or `security.isAccounting()`.
   1. Save this final rule, and add it to your "Security Policy" policy and [re-scan this PR]({{ checks_page_url }}).

<hr>
<h3 align="center">Comment on this Pull Request once you're done, and visit the <a href="{{ route_pr_url }}">next PR</a> to continue.</h3>
