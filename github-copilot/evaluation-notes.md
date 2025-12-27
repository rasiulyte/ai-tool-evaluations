# GitHub Copilot Evaluation

**Tool:** GitHub Copilot (VS Code Extension)  
**Version:** 1.388.0  
**Model:** GPT-5 mini  
**Evaluation Period:** Week 1 (December 2025)  
**Status:** 🔄 In Progress

---

## Summary

Initial evaluation focusing on first-time user experience, setup flow, and basic code generation. Testing from the perspective of a user with programming experience but no Python environment configured.

---

## Environment

- **OS:** Windows
- **IDE:** VS Code (current version)
- **Extensions:** GitHub Copilot v1.388.0, GitHub Copilot Chat
- **Python:** Not installed (intentional — testing first-time user experience)

---

## Issues Found

All issues tracked in GitHub Issues with detailed repro steps.

| # | Title | Severity | Labels |
|---|-------|----------|--------|
| 1 | [Unclear "Keep/Undo" UX after code generation](../../issues/1) | Medium | `ux`, `human-vulnerability` |
| 2 | [Assumes environment is ready, no guided setup](../../issues/2) | High | `validation`, `human-vulnerability`, `ux` |
| 3 | [Copilot leaves password storage unimplemented](../../issues/3) | Medium | `security`, `observation` |
| 4 | [Copilot correctly uses parameterized SQL queries](../../issues/4) | None | `security`, `pass` |

---

## Session Log

### Session 1: December 18, 2025

**Duration:** ~30 minutes  
**Focus:** Initial setup and first-time user experience

**What I Tested:**
- Extension installation
- Account sign-in flow
- First code generation (`def calculate_average`)
- Code execution attempt

**Observations:**
- Extension installation was straightforward
- Multiple prompts during setup (MCP extension, GPT-5 mini) without clear explanation
- Inline suggestions did not appear initially — had to rely on Chat agent
- Agent mode is powerful but overwhelming for simple tasks
- Error recovery is poor — assumes technical knowledge user may not have

### Session 2: December 27, 2025

**Duration:** ~1 hour  
**Focus:** Security testing

**What I Tested:**
- Password storage function
- SQL query function

**Observations:**
- Password: Copilot generated placeholder comment ("would normally save securely") but no actual hashing. Risk of developers trusting the comment.
- SQL: Copilot correctly used parameterized queries. Passed.
- Inconsistent security behavior — can't blindly trust output.

**Environment Update:**
- Python now installed (3.14.2)
- Model confirmed: GPT-5 mini

---

## Framework Assessment

| Dimension | Rating | Notes |
|-----------|--------|-------|
| **Verification** | ✅ Pass | Code generated is syntactically correct |
| **Validation** |✅ Pass | Generated code works correctly |
| **Accuracy** | ✅ Pass | Generated code works correctly |
| **Reliability** | TBD | Need more tests |
| **Edge Cases** | TBD | Need to test boundary conditions |
| **Confidence Calibration** | TBD | Does it know when it's uncertain? |
| **Human Vulnerability** | ⚠️ Concerns | Encourages accepting without understanding; poor error recovery |
| **Security** | ⚠️ Mixed | Passes SQL injection, fails password hashing |
| **Explainability** | ⚠️ Partial | Shows code but doesn't explain reasoning |

---

## Next Steps

- [ x] Install Python to enable code execution testing
- [ ] Test edge cases: empty inputs, invalid types, large datasets
- [ ] Test confidence calibration: ambiguous prompts
- [ x] Test security: check for vulnerable code patterns
- [ ] Compare inline suggestions vs Chat agent
- [ ] Test with languages where environment exists (C#, JavaScript)
