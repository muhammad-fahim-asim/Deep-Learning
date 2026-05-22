# Infix to Postfix Neural Translator

A deep learning proof-of-concept that learns to convert mathematical expressions from human-readable **infix notation** into **postfix notation** (Reverse Polish Notation).

## Overview

This repository contains a notebook-based implementation of a neural model for sequence translation of arithmetic expressions. The model is trained on fully parenthesized expressions built from five identifiers (`a`, `b`, `c`, `d`, `e`) and four operators (`+`, `-`, `*`, `/`).

The goal is to demonstrate how a data-driven model can learn to map infix formulae to equivalent postfix strings, a format that is easier to evaluate using stack-based algorithms.

## Contents

- `Infix_to_postifx_notation_final_solution.ipynb`: Jupyter notebook with data generation, sequence encoding, model training, and example inference.
- `transformer_infix2postfix.weights.h5`: Saved model weights for the trained transformer-style translator.

## Key Concepts

- Infix notation: operators appear between operands (e.g. `a + b`).
- Postfix notation: operators appear after operands (e.g. `a b +`).
- Postfix is unambiguous and well-suited for stack-based evaluation.

## Usage

1. Open `Infix_to_postifx_notation_final_solution.ipynb` in Jupyter Notebook or JupyterLab.
2. Run the notebook cells to generate data, train the model, and test translation examples.
3. Optionally load the saved weights from `transformer_infix2postfix.weights.h5` for inference.

## Notes

- Expressions are generated with a maximum syntactic depth of 3 to keep the training domain manageable.
- The project uses TensorFlow/Keras for model definition and training.
