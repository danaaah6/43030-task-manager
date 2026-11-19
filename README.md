# 43030 Task Manager

Lecture 4 practical (43030 Professional Practice in Computing): a Python task manager with unit tests, packaged in Docker and run by a GitHub Actions CI/CD pipeline. Issues are tracked on a GitHub Projects board.

## Project structure
- `index.html`: report page, updated automatically with tasks and test results
- `Dockerfile`: builds the container that runs the scripts
- `.github/scripts/todo.py`: Task and TaskPool classes
- `.github/scripts/todo-test.py`: unit tests for todo.py
- `.github/scripts/update_index.sh`: writes tasks and test results into index.html
- `.github/scripts/entrypoint.sh`: runs all scripts inside the container
- `.github/workflows/ci.yml`: builds and runs the Docker image on every push to main
- `.github/workflows/tracker.yml`: runs when a pull request is merged
