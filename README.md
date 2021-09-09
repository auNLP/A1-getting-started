[![github actions pytest](https://github.com/auNLP/A1-getting-started/actions/workflows/pytest-cov-comment.yml/badge.svg)](https://github.com/auNLP/A1-getting-started/actions)


# A1: Getting started
An assignment on getting started with pytesting, Github actions and continuous development.

The requirement for the assignment is submitting a working neural network with test included. The tests should
- [ ] that it is able to memorize random 10 examples
- [ ] generalize it to take an input of `range(n, n+5)` and return n, where n is a whole number between 0 and 2
    - you might need to scale the input
- [ ] Classify more than 90% of digit correctly in the MNIST database
- [ ] Test that the networks performance improve over 10 epochs

Potentially:
- [ ] Test that the network trains faster using SGD 

If you werent there for day 3 of the workshop feel free to use the talk to Kenneth to make a deal about the assignment.



## Project Organization
```
├── LICENSE                <- the license of this code
├── README.md              <- The top-level README for this project.
├── .github            
│   └── workflows          <- workflows to automatically run when code is pushed
│   │    └── pytest.yml    <- A workflow which runs pytests upon push
├── tests                  <- The pytest test suite
│   ├── test_numpy.py         
│   └── test_neural_network.py
├── .gitignore             <- A list of files not uploaded to git
├── requirement.txt        <- A requirements file of the required packages.
├── neural_network.py      <- A script containing code for a numpy neural network (currently missing)
└── ...
```

##

## FAQ

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