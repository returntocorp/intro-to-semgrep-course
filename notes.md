

Githubtraining repos
https://github.com/search?o=desc&p=1&q=topic%3Alearning-lab+org%3Agithubtraining+fork%3Atrue&s=forks&type=Repositories

[Building: Events as triggers | GitHub Learning Lab](https://lab.github.com/docs/events)

[Actions | GitHub Learning Lab](https://lab.github.com/docs/actions)

[Building: Using Learning Lab actions | GitHub Learning Lab](https://lab.github.com/docs/using-actions)

[Testing your course | GitHub Learning Lab](https://lab.github.com/docs/testing#test-your-course)

[Choose a topic for your course | Write a Learning Lab course | GitHub Learning Lab](https://lab.github.com/githubtraining/write-a-learning-lab-course)


[github/learning-lab-components: Open sourced components from GitHub Learning Lab](https://github.com/github/learning-lab-components)
* Note: no non Dependabot updates since last Fall :(

[githubtraining/write-a-ll-course: Course repo for Learning Lab course "Write a Learning Lab course".](https://github.com/githubtraining/write-a-ll-course)

[flash - How to embed a video into GitHub README.md? - Stack Overflow](https://stackoverflow.com/questions/4279611/how-to-embed-a-video-into-github-readme-md)


## Errors

* Referencing a branch that doesn't exist in template repo
* Referencing `main` when creating a new PR fails.
  * Why did `welcome` fail and not `setup-semgrep`?
* Referencing a file that doesn't exist in messages
* `{{}}` vs `%var` in different contexts - why?
* Having a responses.md file that references a `{{ variable }}` that isn't sent via a `data`.
* Template repo being too big - there's a max size
* Description cap size at 255
* Online editor IDE deletes all comments
* When you push commits view online editor it doesn't sync the course, you have
  to do that manually

## Building the Course

~~~bash
git checkout -b welcome
~~~

Add the following to README.md at the top

```
This is a fork of Juice Shop being used for Semgrep training. Major thanks to the creators and maintainers!
```

Push branch and create PR.

Title: Welcome to Semgrep! Getting Set Up

Copy in `01_welcome.md` 

Fix a bunch of the copy to remove references to the bot.


# semgrep.yml

## Next Steps

Copy the following YAML into [.github/workflows/semgrep.yml]({{ url }}).

~~~yaml
name: Semgrep
on: [pull_request]
jobs:
  semgrep:
    name: Scan
    runs-on: ubuntu-latest
    env:
      INPUT_PUBLISHURL: https://dev.semgrep.dev
    steps:
      - uses: actions/checkout@v1
      - uses: returntocorp/semgrep-action@v1
        with:
          publishToken: ${{ secrets.SEMGREP_APP_TOKEN }}
          publishDeployment: TODO
~~~    


# Lab steps

🛠️ = user, 🤖 = Lab
🤖 Before - forks vulnerable repo
* Set the Semgrep repo secret
🤖 Set up semgrep.yml
🤖 Issue PR with X == X and watch it fail
🛠️ Change the code to 3 = 5 or something else and have it succeed
🛠️ Walk briefly though Semgrep App - what it does, where things are
* Intro to ellipses operator - block eval(...)
* Intro to metavar
* Warn on new route - audit only
* Create owasp_devslop community Slack channel - point webhook there
* Audit @csrf_exempt or other authn/authz
* XSS
* < write some custom rule and add it to policy >