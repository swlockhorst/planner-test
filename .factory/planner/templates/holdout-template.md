# Holdout Evaluation Scenarios

## Release Information

- **Project:** [Project name]
- **Release:** [Release ID]
- **Title:** [Release name]
- **Status:** Draft
- **Related PRD:** [PRD reference and revision]
- **Revision:** [Holdout revision]
- **Classification:** Confidential — QA Only

## 1. Evaluation Overview

Describe the purpose of the holdout evaluation for this release.

Identify the major capabilities and behaviors being evaluated.

All scenarios must trace to requirements in the approved PRD.

## 2. Evaluation Scenarios

### HOLD-001: [Scenario Title]

**Related Requirements:** REQ-001

**Category:** Functional / Edge Case / Error Handling / Security / Accessibility / Performance / Other

**Priority:** Critical / High / Medium / Low

**Objective:**
Describe the specific behavior or requirement this scenario independently validates.

**Preconditions:**

- Required application state.
- Required accounts, permissions, or configurations.
- Relevant environmental conditions.

**Test Data:**

- Inputs and test fixtures needed for evaluation.
- Boundary values or unusual inputs when relevant.
- Reference to protected test data when appropriate.

**Execution Steps:**

1. [Action or operation]
2. [Action or operation]
3. [Action or operation]

**Expected Results:**

- [Observable outcome]
- [Observable outcome]
- [Conditions that establish success]

**Failure Conditions:**

- [Behavior that constitutes failure]
- [Incorrect or unacceptable outcome]

**Evaluation Method:** Automated / Manual / Hybrid

**Notes:**
Additional information required by the QA evaluator.

Repeat for each holdout scenario.

## 3. Requirement Coverage

Map every holdout scenario to the PRD requirements it validates.

| Requirement | Holdout Scenarios  | Coverage Notes         |
| ----------- | ------------------ | ---------------------- |
| REQ-001     | HOLD-001, HOLD-002 | [Coverage description] |
| REQ-002     | HOLD-003           | [Coverage description] |

Identify critical requirements without sufficient holdout coverage.

Do not invent requirements solely to increase coverage.

## 4. Evaluation Rules

- Evaluate the implementation against the approved PRD.
- Use the defined preconditions, inputs, and expected outcomes.
- Do not modify scenarios to accommodate incorrect application behavior.
- Record actual results and evidence when scenarios are executed.
- Distinguish application failures from evaluation environment failures.
- Do not mark unexecuted or inconclusive scenarios as passed.
- Do not expose private scenario details to coding agents.
- Do not use these scenarios as implementation instructions.
- Report ambiguities or contradictions to the human rather than silently changing expectations.

## 5. Confidentiality and Access

Holdout scenarios must be stored separately from the application repository and normal implementation artifacts.

Access is restricted to:

- The Planning Agent during scenario creation.
- The human responsible for release approval.
- Authorized QA evaluators during validation.

Coding agents, decomposition agents, planning review agents, and GitHub issue publishers must not receive private holdout content.

Never include holdout scenario details in:

- PRDs.
- Design or architecture documents.
- GitHub implementation issues.
- Coding-agent prompts.
- Application source repositories.
- Implementation-facing test reports.

Evaluation feedback provided to coding agents must not disclose private inputs, exact expected results, or other information that would undermine the holdouts.

## 6. Review and Approval

Before release approval, verify:

- [ ] Scenarios trace to approved PRD requirements.
- [ ] Critical requirements have appropriate evaluation coverage.
- [ ] Expected results are objective and verifiable.
- [ ] Preconditions and test data are sufficiently defined.
- [ ] Scenarios do not introduce undocumented requirements.
- [ ] Scenarios do not depend unnecessarily on implementation details.
- [ ] No blocking ambiguities remain.
- [ ] Confidential storage and access restrictions are verified.

## 7. Approval

- **Status:** Draft / Approved
- **Approved By:** [Human]
- **Approval Date:** [Date]
- **Revision:** [Revision identifier]
- **PRD Revision:** [Approved PRD revision]
- **Secure Storage Reference:** [Private reference, not a public URL]

Approved scenarios are sealed against unauthorized modification.

Any change to approved scenarios requires a documented revision and appropriate human authorization.

---

## Document Rules

- Holdouts are independent evaluations, not additional product requirements.
- The PRD defines expected product behavior.
- Holdouts evaluate that behavior using scenarios hidden from coding agents.
- Favor meaningful behavioral coverage over large numbers of redundant tests.
- Include successful, failure, boundary, and adversarial scenarios where relevant.
- Make test outcomes reproducible and objectively measurable.
- Avoid brittle checks tied to unnecessary implementation details.
- Never fabricate evaluation results.
- Never publish actual holdout scenarios to the application repository.
- Never treat this template itself as confidential; only populated scenario content requires protection.
