# Flight Delay Prediction

A machine learning project for predicting flight delay risk using
information available before departure.

## Research Question

Can machine learning reliably estimate the probability of a flight
being significantly delayed using information available before departure?

## Problem

Flight delays affect passengers' travel plans, connections, and schedules.
Passengers are often informed about delays only after uncertainty has
already increased.

Instead of only reporting whether a flight is currently delayed, this
project explores whether machine learning can provide an earlier estimate
of delay risk.

For example:

Flight: AA123  
Scheduled departure: 6:00 PM  
Predicted delay risk: 72%

The idea is similar to a weather forecast: the model communicates risk
rather than claiming with certainty that a delay will occur.

## Machine Learning Task

The problem will initially be formulated as a binary classification task.

Target:

- 0: Departure delay < 15 minutes
- 1: Departure delay >= 15 minutes

The model will output the probability of the positive class.

Example:

P(Delay >= 15 minutes) = 0.72

## Possible Input Features

Only information available before departure should be used.

Examples include:

- Airline
- Origin airport
- Destination airport
- Scheduled departure time
- Day of week
- Month
- Flight distance
- Historical delay patterns

Features containing information that becomes available after departure
will not be used because they would cause data leakage.

## Evaluation

The project will evaluate both prediction performance and the reliability
of predicted probabilities.

Possible metrics include:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix
- Probability calibration

## Project Structure

- `data/` - Raw and processed data
- `notebooks/` - Data exploration and model experiments
- `src/` - Reusable Python code

## Status

Work in progress.