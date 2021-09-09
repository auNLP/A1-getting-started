[![github actions pytest](https://github.com/auNLP/A1-getting-started/actions/workflows/pytest.yml/badge.svg)](https://github.com/auNLP/A1-getting-started/actions)


# A1: Getting started
An assignment on getting started with pytesting, Github actions and continuous development.

The requirement for the assignment is submitting a working neural network with test included. The tests should
- [ ] Classify more than 90% of digit correctly in the MNIST database. This should look something like this:
```
def test_mnist():
    network = NeuralNetwork([784, 30, 10])
    # train and evaluate

    # check that accuracy is above 90%
    assert test_acc >= 0.90

```
*Note*: This is dummy code. It displays the intention. Not the exact form.

- [ ] It can memorize random 10 examples. *Note* that while this is not something we want our network to do in general, it simply shows that the network is able to overfit. Assuming that it couldn't with 20k+ parameters there is probably an error in the code.
```
def test_memorize():
    sample = random.sample(train_data, k=10)
    network = NeuralNetwork([784, 30, 10])

    # train on sample

    # check that classifies all correctly on the same sample
    assert acc == 1
```

- [ ] generalize it to take an input of binary and outputs the corresponding digit. Where the possibles inputs is the number between 0 and 1.
```
def test_binary():
    train, test = generate_binary()
    network = NeuralNetwork([784, 30, 10])

    # train on sample
    # ...
```

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
