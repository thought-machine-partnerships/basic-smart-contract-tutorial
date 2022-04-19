# Basic Smart Contract Tutorial

This tutorial series will introduce you to the concept of Smart Contracts in Vault and to teach you how to write a simple Smart Contract yourself.

A Smart Contract is the representation of the financial logic of a given bank Product. Written in a safe subset of Python, it allows to deterministically describe the behaviour of a Product for all events of its lifecycle.

The first step to writing a smart contract is gathering your requirements and designing how you want your smart contract to operate. For this tutorial, we are going to use a simple Current Account Product with an Overdraft facility. This product will allow the customer to spend money, enter an overdraft and charge them a fee when they withdraw past their overdraft limit nonetheless paying a small amount of interest on positive balances.

## Before You Start

We will be using the `client` object defined in the helper script in this branch to handle API interactions and a suite of simulation tests to test our Smart Contract as we go. Full documentation of these scripts is available on the 'Development and testing' page of your Documentation Hub.

We will be using a script found on this branch, `vault_caller.py`, to allow our tests to talk to a real instance of Vault. We will be using the `client` object defined in the helper script to handle API interactions and a suite of simulation tests to test our Smart Contract as we go.

Before using the script, you must install the following external libraries via [pip](https://pypi.org/project/pip/) or a similar mechanism:

```
python-dateutil
requests
```

Full documentation of the vault caller script is available on the 'Development and testing' page of your Documentation Hub, under the 'Simulation Testing' subheading.

We will also be using the set of unit tests in `simple_tutorial_tests.py`. We will be using them to demonstrate the functionality of the Smart contract we write.

After checking out each exercise, modify `simple_tutorial_tests.py` and ensure that `core_api_url` and `auth_token` are set to the correct values. To learn more about these variables, see the Core API Documentation.

> The unit tests are designed to run with the exercise they are included with. As you progress through the branches of this tutorial, the file will change accordingly, with the API URL and auth token needing to be set each time.

## Exercise Branches

Each of the exercises is set up on a different branch in this repo (`exercise-1`, `exercise-2` etc.). To check out the first exercise, run `git checkout exercise-1`. In order to see a solution to the exercise, run `git checkout exercise-1-solution`. This is the same for exercise 2, 3 and so forth.
