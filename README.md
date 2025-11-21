# NIST Quantum Random Integer Sampling

A tiny Python utility that fetches the latest 512-bit pulse from the **NIST Randomness Beacon** and converts it into **uniform random integers** using rejection sampling — all from **one pulse per call**.

This is meant to be a minimal, easy-to-audit way to grab quantum random numbers from a public beacon.

## What it does

- Pulls the last NIST Beacon pulse (`outputValue`, 512 bits).
- Treats it as a fixed 512-bit pool.
- Produces uniform integers in `[low, high]` via rejection sampling.
- Uses **only that single pulse** (no refills).
