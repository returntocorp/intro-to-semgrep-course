## The Power of Democratizing Static Analysis
One of the *key differentiators* about Semgrep is how easy it is to write custom rules.

This fundamentally changes how you can leverage static analysis to scale your AppSec program.

Rather than being a black box, one-size-fits-all, "I sure hope the vendor built all the use cases I could ever need," single purpose tool, Semgrep is a Swiss army knife and your imagination is the limit.

Yes, there are over 1,000 out-of-the-box security checks you get for free.

But you can also use Semgrep for:
* **Enforcing secure guardrails**: "You should be using our `internal_auth` library for all auth purposes."
* **Just-in-time developer education**: "Hey there, I see you're doing `something dangerous like crypto or parsing XML`, here's how we do it in our company: `link to internal docs`."
* **Enforcing org or code base specific business logic**: "`foo()` should always be called before `bar()`, else it's a bug."
* And much more

As Semgrep rules look just like the code you're targeting (with some helpful abstractions), many **developers** and engineering orgs can write custom rules as well (or better!) than security teams.

Why have separate tools when developers and the security team can solve their respective problems with the same tool! 🤝 

Alright, let's get into it.