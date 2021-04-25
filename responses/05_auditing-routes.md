## Watching but Not Breaking the Build



## Intermediate Rule Writing

Here's a few quick tips, but again, see the Issue for links to the full docs.

### Compose Patterns `pattern-either`

Want your rule to match multiple things? Click the `+` and select `"or is"` one or more times.

These patterns will be considered like a boolean OR - if either match, the Semgrep rule as a whole will match. ([docs](https://semgrep.dev/docs/writing-rules/rule-syntax/#pattern-either))

### Metavariables in messages

When a metavariable you use in a pattern matches a piece of target code, you can reuse that metavariable in the `message` field.

This way you a can give developers (or you) a more useful, actionable, contextual message, by referencing, for example, the function names or variables involved and why there's an issue.

### "and is not" (`pattern-not`)

Like "or is" (`pattern-either`), you can combine multiple `pattern-not` clauses to filter out multiple sets of code patterns you don't want to match ([docs](https://semgrep.dev/docs/writing-rules/rule-syntax/#pattern-not)).

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
<h3 align="center">Congrats, you're done!</h3>