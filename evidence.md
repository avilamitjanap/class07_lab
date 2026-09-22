# Class 07: repository, trigger and image evidence

Use actual output. Replace each blank; do not copy the acceptance text as a result.

## Step 1 — Create the repository and pipeline
- Repository URL: https://github.com/avilamitjanap/class07_lab
- Workflow path: https://github.com/avilamitjanap/class07_lab/tree/main/.github/workflows/ci.yml
- First passing run URL and source commit: https://github.com/avilamitjanap/class07_lab/actions/runs/35757128693    

5e5cc19

- Actual unit-test result: https://github.com/avilamitjanap/class07_lab/actions/runs/35757128693/job/106845600326

Run python3 -m unittest -v
test_above_boundary (test_app.ClassifyTests.test_above_boundary) ... ok
test_below_boundary (test_app.ClassifyTests.test_below_boundary) ... ok
test_endpoints (test_app.ClassifyTests.test_endpoints) ... ok
test_exact_boundary (test_app.ClassifyTests.test_exact_boundary) ... ok
test_invalid_values (test_app.ClassifyTests.test_invalid_values) ... ok

----------------------------------------------------------------------
Ran 5 tests in 0.001s

OK

## Step 2 — Run only on pushes to main
- Commit/run that installed the main-only trigger: 26cc17c Run CI only on main pushes
26cc17c3690c23ee97447a9179ed567de5d8a525

https://github.com/avilamitjanap/class07_lab/actions/runs/35759083223

- `trigger-check` branch commit SHA:a7bb10c472fb8f6b5103aa2a3c4593fd09cffdfd

- What the Actions page showed for that branch/SHA: Filtering actions by trigger-check branch showed no workflow runs. commit a7bb10c was on github but no run was crated for it 
- Run URL after the same commit was pushed to `main`: https://github.com/avilamitjanap/class07_lab/actions/runs/35759701618
- Explain why a local commit alone does not start GitHub Actions:

git commit only writes into the .git folder on mymachine, therefore github doesn't actually know that a commit exists. The push is the event that allows github to receive it, the branch ref moves and github then reads the on rules in ci.yml against that event. If the event matches, in this case the push, then github creates the run.

## Step 3 — Publish and retrieve the Python image
- Package page URL (GHCR, linked to this repository):
- Source commit, run URL and attempt:
- Actual source-test and packaged HTTP test results:
- Complete registry reference (`repository@sha256:` plus 64 hexadecimal digits):
- Platform:
- Exact pull command:
- Actual pulled-image HTTP test output:

## Limits and explanation
- One thing these tests do not establish:
- Explain the difference between the Git repository and its linked image package:
- AI assistance used (tool, task, verification), or `none`:

## Optional failure-and-repair extension
- Failed commit/run, useful assertion and skipped package job:
- Repaired commit/run and recovered digest:

Save the successful package job summary, or paste its release record above.
If using a fallback, explicitly mark the uncompleted hosted checks and local
simulation results. Do not invent a repository, run URL or successful GHCR push.
