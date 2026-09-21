# Week 3 Submission — Individual Readiness Lab

## Student information

- Name: LU ZIYANG
- Student ID: 21321691
- Repository: https://github.com/yixi1120/MAIE6000c-starter-louis
- Checkpoint tag: `w03-readiness`
- Commit SHA: See the commit referenced by the `w03-readiness` tag

## 1. What I changed

I strengthened the Case creation input validation. Leading and trailing whitespace is now
removed before length validation, preventing whitespace-only titles or descriptions from
being accepted and stored as empty values.

## 2. Files touched

- `services/common/schemas.py`
- `tests/integration/test_api_case_flow.py`
- `submissions/week03/README.md`

## 3. How I verified it

- Ran the unit and integration test suite successfully: 7 tests passed.
- Built and started the Docker Compose stack; the API, AI, database, and worker services ran
  successfully, and all services with health checks reported healthy.
- Ran the end-to-end smoke test against the running stack: 1 test passed.
- Ran Ruff successfully.
- Verified that a whitespace-only title returns HTTP 422.
- Verified that a whitespace-only description returns HTTP 422.
- Verified that valid input with surrounding whitespace is normalized before storage.

## 4. Known limitations or notes

This change only normalizes leading and trailing whitespace. It does not modify whitespace
inside otherwise valid titles or descriptions.

## 5. AI Use Statement

I used OpenAI Codex to help inspect the starter repository, identify a bounded validation
issue, and suggest implementation and test cases. I reviewed the proposed changes and
verified the resulting behavior using the automated test suite and Ruff.
