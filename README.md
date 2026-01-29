# Python CI Pipeline 🚀

Educational and hands-on repository to learn **CI/CD with GitHub Actions**, **quality gates using code coverage**, and **infrastructure management with Terraform + Atlantis**, using a **simple but realistic Python project**.

This repository is designed as a **learning lab** and also as a **professional portfolio project**.

---

## 🎯 Project Goals

---

- Enforce **mandatory Pull Requests** into `main`
- Run **automated tests** on every PR
- Measure **code coverage** and block merges if it decreases
- Report **PR coverage and delta vs main**
- Publish coverage reports as artifacts
- Deploy infrastructure using **Terraform**
- Use **Atlantis** for `plan`, `apply`, and rollback
- Learn a complete **CI workflow with GitHub Actions**

---

## 🧱 Repository Structure

```
python-ci-pipeline/
├── .github/workflows/      # GitHub Actions (CI)
├── src/                    # Source code
├── tests/                  # Unit tests
├── terraform/              # IaC
├── .coveragerc             # Coverage
├── requirements.txt        # Dependencies
├── pyproject.toml          # Configuration of project
└── README.md
```

---

## 🐍 Python Project

This Python project is intentionally **simple**, but designed to:

- Require tests
- Include error scenarios
- Allow clear and measurable coverage

The focus is on the **pipeline**, not on domain complexity.

---

## 🧪 Testing & Coverage

- Testing framework: **pytest**
- Coverage: **pytest-cov**

### Run tests locally

```bash
pytest
```

### Run tests with coverage

```bash
pytest --cov=src --cov-report=term-missing
```

### Generate HTML report

```bash
pytest --cov=src --cov-report=html
```

Report is generated at:

```
htmlcov/index.html
```

---

## 🔒 Branch Rules

The `main` branch is protected:

- ❌ No direct pushes allowed
- ✅ All changes must go through Pull Requests
- ✅ Tests and coverage must pass
- ✅ CI must be green

---

## ⚙️ CI with GitHub Actions

CI pipeline:

1. Runs on every PR and push to `main`
2. Installs dependencies
3. Runs tests
4. Calculates coverage
5. Publishes reports as artifacts
6. (Coming soon) compares coverage vs `main`

---

## 🏗️ Infrastructure

This repository includes infrastructure code to learn:

- `terraform plan`
- `terraform apply`
- PR-driven workflow with Atlantis
- Rollbacks via state changes

The goal is **not the infrastructure itself**, but mastering a **real-world workflow**.

---

## 📈 Roadmap

- [x] Base Python project
- [x] Unit tests
- [ ] Basic CI
- [ ] Required coverage
- [ ] Coverage diff per PR
- [ ] PR comments
- [ ] Basic Terraform
- [ ] Atlantis integration
- [ ] Infrastructure rollback

---

## 👩‍💻 Author

**Vanessa Pacheco**  
Software Engineer  
Santiago, Chile  

🔗 [LinkedIn](https://www.linkedin.com/in/vanessa-pacheco-81b02426/)  
💻 [GitHub](https://github.com/vandev23)

---
  
> This project reflects real CI/CD practices used by modern engineering teams.

