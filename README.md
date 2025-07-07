# Route Planning Based on Traffic Noise Using Genetic and A* Algorithms

This project explores intelligent route planning on the IISER Bhopal campus by incorporating traffic noise as a key decision factor. Traditional pathfinding methods often prioritize only distance or time, overlooking environmental stressors like noise pollution. This project addresses that gap by minimizing the combined cost of distance and noise level.

## Project Overview

The system compares two pathfinding approaches:

- **Genetic Algorithm (GA)**: A stochastic optimization technique inspired by natural evolution. It searches for optimal routes by evolving a population of candidate paths through selection, crossover, and mutation. The fitness of each route is computed using a weighted sum of noise and distance.
- ** A* Search Algorithm**: A deterministic graph search algorithm that uses both actual cost and a heuristic to guide the search. In this case, the evaluation function includes both normalized noise levels and distances.

## Data Collection

Noise levels were recorded using audio devices at various locations on the IISER Bhopal campus. These recordings were analyzed using a Short-Time Fourier Transform (STFT) to extract average amplitude values, which served as a proxy for noise. Coordinates and distances between key points were stored in CSV format, and each path was mapped to its corresponding audio data.

## Methodology

1. **Preprocessing**: Geographic data and audio features were linked for each path segment.
2. **Implementation**: 
   - The GA generates random populations of routes, evaluates their fitness, and evolves better paths over generations.
   - The A* algorithm deterministically finds the shortest noise path using an evaluation function that blends noise and distance.

## Results

- **Genetic Algorithm** can yield different routes on each run due to its randomness but generally finds paths with lower average noise.
- **A\*** always gives the same result, optimized for the combined cost metric.

Both algorithms show that incorporating noise data can significantly influence route selection and improve environmental comfort.

## Project Structure

- `codes/`: Contains Jupyter notebooks implementing Genetic and A* algorithms.
- `dataset/`: Includes audio recordings and CSV files for coordinates and distances.
- `report/`: Contains the detailed project report.

