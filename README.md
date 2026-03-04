# Example_3 — Python Unit Testing with pytest

## Overview
This example demonstrates a basic CI pipeline using **pytest** integrated with **Jenkins**.  
The goal is to understand how unit tests are written in Python and how Jenkins automatically runs them on every commit.

## Project Structure
Example_3/
├── Jenkinsfile
├── pyproject.toml
├── src/
│ └── greeter/
│ ├── init.py
│ └── greeter.py
└── tests/
├── init.py
└── test_greeter.py