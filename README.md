# WordPress Vulnerability Reverser
## Goal

Automatically collect newly published WordPress plugin and theme vulnerabilities
and perform patch analysis.

The tool identifies publicly disclosed vulnerabilities that satisfy:

- CVSS Score > 7.0
- Severity High or Critical
- WordPress Plugin
- WordPress Theme
- Unauthenticated
- Not admin-only

For each vulnerability the tool

1. Collects advisory information.
2. Identifies the GitHub repository.
3. Downloads the vulnerable source.
4. Finds the fixing commit.
5. Generates a patch analysis.
6. Produces a vulnerability report.
7. Produces a reproduction template describing the vulnerable request and affected parameters for use in an authorized test environment.

---

## Workflow

Fetch Latest CVEs


Filter WordPress


Filter High/Critical


Filter CVSS > 7


Reject Admin-only


Reject Authenticated


Locate GitHub


Clone Repository


Locate Fix Commit


Analyze Patch


Generate Report

---

## Output

reports/

    CVE-XXXX/

        advisory.md

        vulnerability.md

        timeline.md

        diff.md

        patch.md

        reproduction.md

---

## Data Sources

NVD

GitHub

Wordfence Advisories

Patchstack

WPScan Database

---

## Patch Analysis

The analyzer identifies

Changed files

Added validation

Nonce verification

Capability checks

Input sanitization

Output escaping

Authorization checks

REST endpoint changes

AJAX endpoint changes

Route registration

Parameter validation

SQL changes

Filesystem changes

File upload validation

---

## Report Contents

Summary

Affected versions

Fixed versions

CVSS

CWE

Attack Vector

Affected endpoint

Affected parameter

Root cause

Fix explanation

Patch explanation

Reproduction template

References
