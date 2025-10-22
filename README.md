# Pro Analytics 02 Python Repository

---

## WORKFLOW 1. Set Up Your Machine

Proper setup is critical.
I completed each step in the following guide and verified carefully.

- [SET UP MACHINE](./SET_UP_MACHINE.md)

---

## WORKFLOW 2. Set Up Your Project

After I verifyied my machine is set up, I set up a new Python project by copying the template from Dr. Case.

- [SET UP PROJECT](./SET_UP_PROJECT.md)

---

## WORKFLOW 3. Daily Workflow

When working on a project, we open just that project in VS Code.


### 3.1 Git add-commit-push to GitHub

Anytime I make working changes to code I git add-commit-push to GitHub.

1. Stage your changes with git add.
2. Commit your changes with a useful message in quotes.
3. Push your work to GitHub.

```shell
git add .
git commit -m "describe your change in quotes"
git push -u origin main
```

### 3.2 Updated All Dependencies and Ran Tests

Used the following code to run tests on file 
```
uv sync --extra dev --extra docs --upgrade
uv cache clean
git add .
uvx ruff check --fix
uvx pre-commit autoupdate
uv run pre-commit run --all-files
git add .
uv run pytest
```

Built documents, fixed errors, and tested them locally using the following code 

uv sync --extra docs --upgrade
uv run mkdocs build --strict
uv run mkdocs serve


### 3.3 Confirm Interpreter 

Confirmed I populated .venv as my vs code interpreter 