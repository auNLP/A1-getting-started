# A1-getting-started
An assignment on getting started with pytesting, Github actions and continuous development.



## Github actions

### Workflows


<br /> 

</details>

<details>
  <summary> Pytest: How do I test the code and run the test suite?</summary>

To run the test suite (pytests) you will need to install the required dependencies. This can be done using 


```
pip install -r requirements.txt
pip install pytest

python -m pytest
```

which will run all the test in the `tests` folder.

Specific tests can be run using:

```
python -m pytest path/to/test_script.py
```

**Code Coverage**
If you want to check code coverage you can run the following:
```
pip install pytest-cov

python -m pytest --cov=.
```


</details>