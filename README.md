# Basic Smart Contract Tutorial

> This series is designed for Vault version 4.0 and later.

This tutorial series will introduce you to the concept of Smart Contracts in Vault and to teach you how to write a simple Smart Contract yourself.

A Smart Contract is the representation of the financial logic of a given bank Product. Written in a safe subset of Python, it allows to deterministically describe the behaviour of a Product for all events of its lifecycle.

The first step to writing a smart contract is gathering your requirements and designing how you want your smart contract to operate. For this tutorial, we are going to use a simple Current Account Product with an Overdraft facility. This product will allow the customer to spend money, enter an overdraft and charge them a fee when they withdraw past their overdraft limit nonetheless paying a small amount of interest on positive balances.

## Prerequisites

This tutorial assumes a working knowledge of [Python](https://www.python.org/) and [Git](https://git-scm.com/). For Python, you should be familiar with writing functions, annotations and how unit tests work. For Git, you should be familiar with cloning a repository and switching between branches.

You will also need to install the following:

- Python 3
- Pip
- An Integrated Development Environment (IDE). Popular choices include [VSCode](https://code.visualstudio.com/), [IntelliJ IDEA](https://www.jetbrains.com/idea/) or [Pycharm](https://www.jetbrains.com/pycharm/), or [neovim](https://neovim.io/) if you're feeling brave.

## Documentation

Each instance of Vault comes with a URL for the Documentation Hub, which contains the relevant documentation for the version of Vault you're working with. If possible, refer to your own Documentation Hub for reference. The tutorial contains links for the public-facing Documentation Hub, which is likely (but not guaranteed) to also work for your version of Vault.

The username and password for the public-facing Documentation Hub is available upon request.

## Cloning the Repo

To follow along with this tutorial, you will need to clone this repo to your local machine. Using a method of your choice, clone this repo to a location of your choosing.

For example, navigate your terminal to somewhere like `~/Documents`, then run `git clone https://github.com/thought-machine-partnerships/basic-smart-contract-tutorial.git`

## Next Steps

Each of the exercises is set up on a different branch in this repo (`exercise-1`, `exercise-2` etc.). To check out the first exercise, run `git checkout exercise-1`.
