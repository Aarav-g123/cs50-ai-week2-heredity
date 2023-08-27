# CS50 Introduction to AI with Python - Week 2: Heredity

## Genetic Trait Likelihood Assessment AI

This program, **heredity.py**, is designed to assess the likelihood that a person will have a specific genetic trait, particularly focusing on the case of hearing impairment caused by the mutated GJB2 gene. The program utilizes Bayesian Network modeling to represent the relationships between genetic information and observable traits. By analyzing family genetics data, the AI calculates the probability of a person inheriting and expressing a given genetic trait.

## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [Bayesian Network](#bayesian-network)
- [License](#license)

## Introduction

Mutated versions of the GJB2 gene can lead to hearing impairment, and each person carries two versions of the gene. The program's objective is to estimate the likelihood of having 0, 1, or 2 copies of the mutated GJB2 gene based on the provided family genetics data. This estimation involves considering not only the direct presence of the mutated gene but also the observed traits, as individuals with the same gene configuration might exhibit different traits.

## Usage

To run the program, execute the following command in the terminal:

```shell
python heredity.py data/familyX.csv
```

Replace `familyX.csv` with the appropriate dataset (e.g., `family0.csv`, `family1.csv`, or `family2.csv`).

## Bayesian Network

The core of this program revolves around the concept of Bayesian Networks, which is a graphical model that represents probabilistic relationships between variables. In the context of heredity, the network encodes dependencies between an individual's gene configuration and their observed traits.

Each individual is represented by two random variables:
- **Gene**: Represents the number of copies (0, 1, or 2) of a specific gene an individual has.
- **Trait**: Represents whether the individual expresses the related trait (e.g., hearing impairment) based on their gene configuration.

The Bayesian Network includes arrows connecting these variables to illustrate the dependencies. For instance:
- An arrow from an individual's Gene variable to their Trait variable indicates that the gene configuration influences the probability of expressing the trait.
- Arrows from the Gene variables of parents to their child's Gene variable signify the hereditary relationship between parents and their offspring.

By constructing and analyzing this network, the program computes the probabilities of different gene configurations and trait expressions within a family.

## License

This program is licensed under the **MIT License**. You can find the full license text in the [LICENSE](LICENSE) file.

---

*Note: This README provides a brief overview of the heredity program and its functionalities. For in-depth technical details, refer to the source code and related documentation.*
