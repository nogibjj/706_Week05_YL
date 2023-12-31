[![CI](https://github.com/nogibjj/706_Week01_YL/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/706_Week01_YL/actions/workflows/cicd.yml)

# 706_Week05_YL

This repository includes the main tasks for Week 05:

* `Makefile` is a configuration file used in Unix-based systems for automating tasks and building software. It contains instructions and dependencies for compiling code, running tests, and other development tasks.
* `.devcontainer` includes a Dockerfile and `devcontainer.json`. The `Dockerfile` within this folder specifies how the container should be built, and other settings in this directory may control development environment configurations.
* `Workflows` includes GitHub Actions, which contain configuration files for setting up automated build, test, and deployment pipelines for your project.
* `.gitignore` is used to specify which files or directories should be excluded from version control when using Git.
* `README.md` is the instruction file for the readers.
* `main.py` is a Python file that contains the main function.
* `test_main.py`  is a test file for `main.py` that can successfully run in IDEs.
* `requirements.txt` is to specify the dependencies (libraries and packages) required to run the project.
* `mylib` contains the scripts for extracting, querying, transforming and loading the database file `GroceryDB_IgFPro.csv`: `extract.py`, `query.py`, `transform_load.py`.

## Project description

Create a Python script that interacts with a SQL database `GroceryDB`, with CRUD functions: Create, Read, Update, and Delete operations on `GroceryDB` database. It uses `SQLite3` for database interaction and `PrettyTable` to display query results in tabular form.

I used 3 queries:

* `Query 1`: selects all the rows from `GroceryDB` table and displays the top 5 rows.

`SELECT * FROM GroceryDB LIMIT 5 OFFSET 1`

* `Query 2`: updates the `count_products` column of `GroceryDB` table for the row with `general_name` as `arabica coffee`.

`UPDATE GroceryDB SET count_products = 100 WHERE general_name = arabica coffee`

* `Query 3`: deletes the row from `GroceryDB` table with `general_name` as `arabica coffee`.

`DELETE FROM GroceryDB WHERE general_name = arabica coffee`


## Project environment

* Use codespace for scripting
* Container built in `devcontainers` and virtual environment activated via `requirements.txt`
* To run the code, use the command `python main.py` in the terminal
* To test the code, use the command `python -m unittest test_main.py` in the terminal

## Workflow

![Alt text](figures/ETL_workflow.png)

## Check format & errors

1. make format

2. make lint

![Alt text](figures/lint.png)

3. make test

![Alt text](figures/test.png)

## Reference

https://github.com/nogibjj/sqlite-lab