# Spaceship Titanic

A machine learning project for the Kaggle **Spaceship Titanic** competition.

- **Competition:** https://www.kaggle.com/competitions/spaceship-titanic
- **Competition type:** Getting Started (rolling leaderboard)
- **Task type:** Binary classification on tabular data

## Problem Statement

It is the year 2912. The Spaceship Titanic, an interstellar passenger liner launched a month ago, was carrying almost 13,000 passengers to newly habitable exoplanets orbiting nearby stars. While rounding Alpha Centauri on its way to its first destination, the torrid 55 Cancri E, the ship collided with a spacetime anomaly hidden inside a dust cloud. Although the ship stayed intact, nearly half of the passengers were transported to an alternate dimension.

To help the rescue crews recover the lost passengers, the task is to **predict which passengers were transported by the anomaly**, using personal records recovered from the ship's damaged computer system.

Given a passenger's details (home planet, cabin, destination, age, spending on onboard amenities and so on), predict whether the passenger was transported (`True`) or not (`False`).

## Evaluation

Submissions are evaluated on **classification accuracy**: the percentage of passengers whose `Transported` value is predicted correctly.

## Submission Format

The submission file must be a CSV with a header row, one row per passenger in the test set, and a `True` or `False` prediction for each:

```
PassengerId,Transported
0013_01,False
0018_01,False
0019_01,False
...
```

## Dataset

The dataset consists of passenger records provided as CSV files. The files are **not** stored in this repository. See [`data/README.md`](data/README.md) for a full description of the files and columns, and how to download them.

## Status

Work in progress. This README currently covers the problem definition only.