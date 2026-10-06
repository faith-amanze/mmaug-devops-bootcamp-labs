# Lab 01 Evidence



- Pull requests: #4 https://github.com/faith-amanze/mmaug-devops-bootcamp-labs/pull/4

  and #5 https://github.com/faith-amanze/mmaug-devops-bootcamp-labs/pull/5

- Failed run URL: https://github.com/faith-amanze/mmaug-devops-bootcamp-labs/actions/runs/37465958152/job/112276913771

- Later successful run URL: https://github.com/faith-amanze/mmaug-devops-bootcamp-labs/actions/runs/37477728324 (run #10, commit 6c7deae, PR #5 after the repair)

- Deployed Pages URL: https://faith-amanze.github.io/mmaug-devops-bootcamp-labs/



**Exercise 2:** No. The "Keep the build artifact" step has no `if:` condition,

so it uses the default `success()` check. In failed run #9, **Run unit tests**

failed, and **Build deployable artifact** and **Keep the build artifact** were

skipped, so no artifact was uploaded.



**Gate:** The deploy job needs the validate-and-build job, so nothing is

deployed unless lint and tests pass.



**Exercise 5:** The artifact's `build-info.json` records the same commit and

run number as the workflow run, so a deployed build can be traced to its

source revision.

