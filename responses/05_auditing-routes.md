## Watching but Not Breaking the Build



## Intermediate Rule Writing

### pattern-either

### Metavariables in messages

### pattern-not



## ⌨️ Activity: Auditing Routes

We're going to start simple, matching just a few routes, and then we'll iteratively improve our rule to make it more precise.

Your rule will largely be the same each time (with some improvements). The reason I'm providing different links in each is because I've changed the comment annotations to make it clear which lines you should and shouldn't be matching.

1. Update [this rule]({{ route_get_playground_url }}) to only match GET routes (`app.get()`).
2. Update [this rule]({{ route_all_playground_url }}) to now match all PUT, POST, and DELETE routes as well.
3. Update [this rule]({{ route_use_playground_url }}) to also include `app.use`, but only when the first argument is a string literal (the path). Include the matched path for any route, regardless of HTTP verb, in the return message.
4. Update [this rule]({{ route_use_playground_url }}) to be the above, but only include routes that don't do *any* auth, that is, don't call `security.denyAll()`, `security.isAuthorized()`, or `security.isAccounting()`.
   1. Save this final rule, and add it to your "Security Policy" policy and [re-scan this PR]({{ checks_page_url }}).

<hr>
<h3 align="center">Visit the <a href="{{ route_pr_url }}">next PR</a> to continue.</h3>