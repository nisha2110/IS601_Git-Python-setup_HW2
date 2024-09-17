# Homework2 Project Setup
## Specifically, I set up:

Python Virtual Environments: Essential for managing project-specific dependencies.
Pytest: A powerful framework for writing and running Python tests.
Pylint: A tool for analyzing your Python code for errors and enforcing a coding standard.
Coverage: A tool for measuring the coverage of your unit tests.
Git: To practice version control techniques such as branching, merging, and using stash.
Additionally, we will delve into integrating these tools with Visual Studio Code (VSCode) and Windows Subsystem for Linux (WSL 2), enhancing your ability to manage development tasks.

## Instructions:
1. Create directory and use touch command create files.
    
    mkdir ProjectSetup_HW2
    touch readme.md
    touch .gitignore
    makdir calculator
    makdir tests
    touch calculator/__init__.py
    touch tests/__init__.py
    touch tests/tests_calculator.py
    touch pylintrc
    touch pytest.ini

2. Install python virtual environment, so we can manage the virtual environment to issolate your dependences from the global version of python. we need to do this once for your computer, this is a global python package.   
    
    sudo apt install python3-virtualenv
    mkdir venv
    virtualenv -p /usr/bin/python3 venv

3.  Go to venv folder and active virtual environment below command:
    source venv/bin/activate

4. Once the virtual environment is a active then install the python dependencies using  pytest, coverage and requirement.txt     
    pip install pytest
    pip install pytest-cov
    pip install -r requirements.txt

5. we can try do this save all our python libraries with current version into requirements.txt file.
    pip freeze > requirements.txt

Note When someone copies / clones your repository they will install the specfic library / dependency requirements for your project using the command:

    pip install -r requirments.txt

6. Finally, Open VScode and test code.
    code .    

## Testing

1. pytest
2. pytest --pylint
3. pytest --pylint --cov

## Output: 

     pytest --pylint
/home/hpatel/Webdeploy_projects2024/ProjectSetup_HW2/venv/lib/python3.8/site-packages/pytest_pylint/plugin.py:223: PytestRemovedIn9Warning: The (path: py.path.local) argument is deprecated, please use (file_path: pathlib.Path)
see https://docs.pytest.org/en/latest/deprecations.html#py-path-local-arguments-for-hooks-replaced-with-pathlib-path
  def pytest_collect_file(self, path, parent):
======================================================================== test session starts =========================================================================
platform linux -- Python 3.8.10, pytest-8.3.3, pluggy-1.5.0 -- /home/hpatel/Webdeploy_projects2024/ProjectSetup_HW2/venv/bin/python
cachedir: .pytest_cache
rootdir: /home/hpatel/Webdeploy_projects2024/ProjectSetup_HW2
configfile: pytest.ini
testpaths: tests
plugins: pylint-0.21.0, cov-5.0.0
collected 4 items                                                                                                                                                    
--------------------------------------------------------------------------------
Linting files
.......
--------------------------------------------------------------------------------

tests/__init__.py::PYLINT PASSED                                                                                                                     [ 25%]
tests/test_calculator.py::PYLINT PASSED                                                                                                                     [ 50%]
tests/test_calculator.py::test_addition PASSED                                                                                                                     [ 75%]
tests/test_calculator.py::test_subtraction PASSED                                                                                                                     [100%]

