![CI](https://github.com/vandev23/python-ci-pipeline/actions/workflows/ci.yml/badge.svg)
![Coverage](https://codecov.io/gh/vandev23/python-ci-pipeline/branch/main/graph/badge.svg)


# 🧪 Python CI Pipeline with Coverage

This repository demonstrates a **production-ready Python CI pipeline** using **GitHub Actions**, focused on clean code, test coverage, and pull request quality gates.

It is designed as a **learning + portfolio project**, showing how modern teams enforce quality before merging to `main`.

---

## 🚀 What This Repository Achieves

- ✅ Pull Requests are **mandatory** to merge into `main`
- 🧪 Tests are required and executed automatically
- 📊 Test **coverage is calculated and enforced**
- 💬 Coverage percentage is **reported directly on PRs**
- 🔒 Branch protection via **GitHub Rulesets**
- 📦 Simple, clean Python project structure

---

## 🧱 Project Structure

```
.
├── src/
│   └── calculator.py
├── tests/
│   └── test_calculator.py
├── .github/
│   └── workflows/
│       └── python-ci.yml
├── requirements.txt
└── README.md
```

---

## 🧪 Testing & Coverage

Tests are written using **pytest**, and coverage is measured with **pytest-cov**.

### Run tests locally

```bash
pytest --cov=src --cov-report=term-missing
```

This will:
- Run all tests
- Show **line-by-line coverage** in the terminal
- Highlight missing lines

---

## 🤖 Continuous Integration (GitHub Actions)

Every **pull request** and **push to `main`** triggers the CI workflow.

The CI pipeline performs:
1. Checkout repository
2. Set up Python environment
3. Install dependencies
4. Run tests with coverage
5. Generate `coverage.xml`
6. Post coverage percentage as a PR comment

### Example PR Comment

```
🧪 Test Coverage
📊 Coverage: 92.45%
```

---

## 🔒 Branch Protection & Ruleset

The `main` branch is protected using **GitHub Rulesets**:

- ❌ Direct pushes to `main` are blocked
- ✅ Pull Request required
- ✅ CI workflow **must pass** before merge
- ⏳ Merges are blocked until all checks succeed

This simulates a **real production workflow**.

---

## 📊 Coverage Visibility Strategy

Current setup:
- ✔️ Coverage shown in CI logs
- ✔️ Coverage reported in PR comments

Planned enhancements:
- 📈 Upload HTML coverage report as CI artifact
- 🧷 Optional link from README to latest coverage report

---

## 🛠️ Tech Stack

- Python 3.9
- pytest
- pytest-cov
- GitHub Actions
- GitHub Rulesets

---

## 🎯 Why This Project Matters

This repository demonstrates:
- Clean CI/CD fundamentals
- Quality gates enforced at PR level
- Test-driven mindset
- Real-world DevOps practices

Ideal as a **portfolio project** for backend, platform, or DevOps roles.

---

## ⏭️ Next Steps

- Add Terraform + Atlantis workflow
- Enforce minimum coverage threshold
- Add CI badges
- Add rollback strategy documentation

---

✨ Built with a focus on learning, quality, and real-world engineering practices.

