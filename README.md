# Trusto Hybrid Biometric Smart Contracts (HBS) Library

The HBS library provides key services for Trusto network:

*   biometric key signing services
*   transaction validation
*   smart contracts storage and execution

It uses both Trusto Hybrid Biometric Blockchain protocol and Trusto Biometric
Document Blockchain protocol libraries to store, validate and execute transactions.

It implements the execution engine and the run time services of the trusto's smart
contracts description language which is a touring complete, declarative, functional
language featuring immutable state and formal verification of the contract rules
correcteness.

## Installation

The only supported installation method, right now, is from source files,
[stack](http://www.haskellstack.org/).

## Building from source

### Prerequisites

You will need to [download and install stack](https://docs.haskellstack.org/en/stable/README/#how-to-install).

You also need [git](https://git-scm.com/) to get the latest source code.

Download and install [Trusto Hybrid Biometric Blockchain protocol library](http://github.com/trusto/hbs) and
[Trusto Document Biometric Blockchain protocol libraries](http://github.com/trusto/bdb).


### Get the source

    git clone https://github.com/trusto/hbs.git
    
### Building

To build the project, you need first to run `stack setup`. This command
will make sure you have the correct haskell compiler, and, if you don't
have it, it will download and install one in a separate location in such
a way to not interract with your existing haskell environment (if you have one):

    #> cd /the/location/of/trusto/hbs
    #> stack setup
    
After the setup (you only need to run setup once) you may build, test or install
the software. To build, simply issue:

    #> stack build
    
To run the tests:

    #> stack test
    
To install it in the stack's install directory, type:

    #> stack install

## Architecture

The biometric blockchain smart contracts library provides:

*   biometric key signing services
*   smart contracts runtime supporting the execution of smart contracts
*   smart contracts execution engine
*   transactions validation engine for hybrid biometric blockchain

## The biometric key

The library provides access to biometric key signing services. It does not implement the biometric
key, but rather access them from an external service provider, perhaps a hardware device.

## The smart contracts runtime

The runtime provides the implementation of services available for contracts, like accessing the transaction
and document blockchains.

## The smart contracts execution engine

It executes the smart contract code. It uses the smart contracts runtime to provide access to different services.

## The transaction validation service

The Trusto Hybrid Biometric Blockchain validates trasactions using smart contracts code. The code is stored in the
document blockchain, and the transaction validation service uses the document hash in the document blockchain to
locate and run the validation code.
