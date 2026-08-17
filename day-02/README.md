# Day 2 — ETA Prediction Systems

## Problem

Design production-grade ETA prediction systems for two related but
fundamentally different settings:

1. Uber-style rider and driver transportation
2. DoorDash/Swiggy-style food delivery

## Core distinction

An Uber-style ETA is primarily a route and travel-time problem:

> Routing ETA + learned residual correction

A food-delivery ETA is an end-to-end fulfillment problem:

> Preparation + courier synchronization + pickup + travel + batching +
> uncertainty

The prediction target, state transitions, available features, and sources of
delay determine the architecture—not the fact that both outputs are called an
ETA.

## System designs

### Uber-style rider/driver ETA

- [Uber ETA ML System Design](./uber-eta/uber-eta-ml-system-design.pdf)

The design starts with a routing baseline and learns its residual error. It
covers map matching, geospatial and real-time features, model complexity and
latency, asymmetric and uncertainty-aware losses, event-driven refresh,
streaming features, delayed labels, monitoring, and graceful degradation.

### Food-delivery ETA

- [Food Delivery ETA ML System Design](./food-delivery-eta/food-delivery-eta-ml-system-design.pdf)

The design treats fulfillment as overlapping, state-dependent clocks. It
models restaurant readiness, courier assignment and synchronization, pickup,
travel, batching, and handoff before composing a calibrated customer promise.
It compares specialized GBDTs with multi-task shared representations and
semantic prediction heads.

## Key concepts

- ETA decomposition and state-machine modeling
- Routing baselines and residual learning
- Point-in-time correct features and labels
- Real-time features, freshness contracts, and event ordering
- Specialized models and multi-task learning
- Asymmetric, robust, and quantile losses
- Calibration and prediction intervals
- Dynamic refresh with displayed-ETA stability
- Low-latency inference, caching, and graceful degradation
- Offline, online, product, business, and system metrics
- Monitoring, failure modes, and production trade-offs

## Key takeaway

Do not begin with “Which model should predict ETA?” Begin with “Which events
and processes cause this outcome?” The decomposition of the real-world process
drives the ML formulation and system architecture.
