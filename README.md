# Basic Smart Contract Tutorial

> This series is designed for Vault version 4.0 and later.

This tutorial series will introduce you to the concept of Smart Contracts in Vault and to teach you how to write a simple Smart Contract yourself.

A Smart Contract is the representation of the financial logic of a given bank Product. Written in a safe subset of Python, it allows to deterministically describe the behaviour of a Product for all events of its lifecycle.

The first step to writing a smart contract is gathering your requirements and designing how you want your smart contract to operate. For this tutorial, we are going to use a simple Current Account Product with an Overdraft facility. This product will allow the customer to spend money, enter an overdraft and charge them a fee when they withdraw past their overdraft limit nonetheless paying a small amount of interest on positive balances.

## Documentation

Each instance of Vault comes with a URL for the Documentation Hub, which contains the relevant documentation for the version of Vault you're working with. If possible, refer to your own Documentation Hub for reference. The tutorial contains links for the public-facing Documentation Hub, which is likely (but not guaranteed) to also work for your version of Vault.

The username and password for the public-facing Documentation Hub is available upon request.

## Before You Start

We will be using the `client` object defined in the helper script in this branch to handle API interactions and a suite of simulation tests to test our Smart Contract as we go. Full documentation of these scripts is available [here](https://documentation.external.thoughtmachine.io/reference/contracts/development_and_testing/).

We will be using a script found on this branch, `vault_caller.py`, to allow our tests to talk to a real instance of Vault. We will be using the `client` object defined in the helper script to handle API interactions and a suite of simulation tests to test our Smart Contract as we go.

Before using the script, you must install the following external libraries via [pip](https://pypi.org/project/pip/) or a similar mechanism:

```
python-dateutil
requests
```

Full documentation of the vault caller script is available on the 'Development and testing' page of your Documentation Hub, under the 'Simulation Testing' subheading.

We will also be using the set of unit tests in `simple_tutorial_tests.py`. We will be using them to demonstrate the functionality of the Smart contract we write.

## Testing Solutions

Each exercise branch comes with a file named `simple_tutorial_tests.py`. We will be using this to demonstrate the functionality of the Smart contract we write. This will contain a different test for each exercise, but it can be run for every exercise using the command

```
python3 -m unittest simple_tutorial_tests <CORE_API_URL> <AUTH_TOKEN>
```

Where `<CORE_API_URL>` and `<AUTH_TOKEN>` are the Core API URL and the Authentication Token for your instance of Vault respectively. To learn more about these variables, see the Core API Documentation.

## Exercise Branches

Each of the exercises is set up on a different branch in this repo (`exercise-1`, `exercise-2` etc.). To check out the first exercise, run `git checkout exercise-1`. In order to see a solution to the exercise, run `git checkout exercise-1-solution`. This is the same for exercise 2, 3 and so forth.
