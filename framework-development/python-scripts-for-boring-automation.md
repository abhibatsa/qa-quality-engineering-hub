# Python Scripts to Automate the Boring Stuff

**Read time:** 4 min

---

Not every automation win requires a full test framework — a lot of a QA
team's time goes to genuinely small, repetitive tasks that a short
Python script eliminates entirely. This is the category of "automation"
that gets overlooked in favor of test-framework work, despite often
having the fastest time-to-value.

## File handling: bulk-renaming/organizing test evidence

Screenshots, logs, and reports pile up fast during a testing cycle.

```python
import os
from datetime import datetime

def organize_test_evidence(source_dir, dest_dir):
    """Move today's screenshots into a dated folder, renamed with a timestamp."""
    today_folder = os.path.join(dest_dir, datetime.now().strftime("%Y-%m-%d"))
    os.makedirs(today_folder, exist_ok=True)
    for filename in os.listdir(source_dir):
        if filename.endswith(".png"):
            timestamp = datetime.now().strftime("%H%M%S")
            new_name = f"{timestamp}_{filename}"
            os.rename(os.path.join(source_dir, filename), os.path.join(today_folder, new_name))
```

## Report parsing: pulling a summary from a raw test report

Extracting pass/fail counts from an XML/JSON report without opening a
GUI tool every time.

```python
import xml.etree.ElementTree as ET

def summarize_junit_report(xml_path):
    tree = ET.parse(xml_path)
    root = tree.getroot()
    total = int(root.get("tests", 0))
    failures = int(root.get("failures", 0))
    errors = int(root.get("errors", 0))
    print(f"Total: {total} | Passed: {total - failures - errors} | Failed: {failures} | Errors: {errors}")
```

Small, but this is the kind of script that turns "let me open Jenkins and
click through the report" into a one-line terminal command — genuinely
saves meaningful time run daily across a team.

## Environment setup: checking prerequisites before a test run

A surprisingly common source of wasted time is starting a test run
against a misconfigured environment and discovering it 20 minutes in.

```python
import requests

def check_environment_ready(base_url, required_services):
    for service in required_services:
        try:
            resp = requests.get(f"{base_url}/{service}/health", timeout=5)
            status = "OK" if resp.status_code == 200 else f"FAIL ({resp.status_code})"
        except requests.exceptions.RequestException:
            status = "UNREACHABLE"
        print(f"{service}: {status}")
```

Run this as the first step of any test cycle — fail fast on an
environment problem instead of discovering it mid-suite.

## CI helper scripts: cleaning up before/after a run

```python
import shutil, os

def clean_previous_run_artifacts(paths_to_clean):
    for path in paths_to_clean:
        if os.path.exists(path):
            shutil.rmtree(path)
            print(f"Cleaned: {path}")
```

Prevents the class of flaky failures caused by stale artifacts from a
previous run bleeding into the current one — a small script, a real
category of bug it prevents.

## Best Practices

- Keep these scripts in a shared team repo/utility folder, not on one
  person's laptop — the whole point is eliminating repeated manual work
  *for the team*, not just for whoever wrote the script
- Write them defensively (handle missing files, unreachable services)
  even though they're "just small scripts" — a script that crashes on
  an edge case at 8am before a release is a bad way to start the day
- Don't over-invest polish here — these are utility scripts, not
  production code; readable and reliable is the bar, not architecturally
  elegant

---
*Part of [QA, Quality Engineering & Quality Management Hub](../README.md) → [Framework Development & Design Patterns](./README.md)*
