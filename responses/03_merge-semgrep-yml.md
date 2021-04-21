Great! Now we're going to set up Semgrep scanning every PR via GitHub actions by creating a `semgrep.yml` in TODO

Though we're going to be using GitHub Actions in this workshop, because Semgrep is nice 
and portable, easily runnable as a standalone binary or Docker, it's pretty easy to set up
Semgrep in pretty much any CI platform under the sun. 

See [these docs](https://semgrep.dev/docs/sample-ci-configs/) for info about setting up 
Semgrep in GitLab, Buildkit, CircleCI, or other providers, and 
[see here](https://semgrep.dev/docs/semgrep-ci/#semgrep-ci) for 

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

