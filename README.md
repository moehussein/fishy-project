# Fishbowl Evolution

Simulating the development of fish intelligence within a controlled environment using neuroevolution and genetic algorithms.

# Operational Mechanism
## The Fish

Fish are housed in an aquarium equipped with a randomly initialized neural network as their cognitive center. Their growth hinges on consuming encountered food items.

## Fish actions include:

    Pulsing (increasing speed akin to a jellyfish) - automatic,
    Splitting (when mature enough to reproduce) - automatic, or
    Turning left/right.

Yet, each cycle drains their energy (and mass) due to cognitive processes, respiration, etc., amplified during movement. If a fish is too small, it perishes, becoming sustenance.
The Food

The fishbowl also harbors food (plankton), which proliferates independently and divides when reaching a certain size.

The Simulation:

The program executes the simulation until all but one fish perish. Then, it resets, introducing a new generation derived from the most successful fish of the prior one.

Observe the behavioral shifts in fish as their neural networks evolve. Initial food abundance and simulation duration per generation also mold the evolution.
Key Features

    Genome retention in browser cache for resuming evolution upon reloading.
    Display of statistics (neural network response distribution, network complexity, and generation durations).
    Customization options include simulation speed, maximum generation duration, and initial food quantity.
    Vision training mode facilitates accelerated improvement in fish vision/steering coordination.
    Load pretrained network feature offers a brain adept at steering fish toward nearby food.

# Fish Brain Mechanics

Fish brains employ LiquidCarrot, a JavaScript implementation of the NEAT algorithm, for rapid neuroevolution and autonomous neural network development.

    LiquidCarrot: [GitHub Repository](https://github.com/liquidcarrot/carrot)
    NEAT: [Exploration Article](https://www.oreilly.com/radar/neuroevolution-a-different-kind-of-deep-learning/)

## Inputs to the Fish Brain

    1st node: Fish speed
    2nd node: Smell - food density in fish vicinity
    3rd node: Distance to nearest food item within fish's visual range
    4th node: Angle to said food item

## Outputs from the Fish Brain

Single node indicating fish rotation angle.

# Observed Evolutionary Patterns

    Abundant food prompts fish to maneuver in distorted circular patterns, striving to gather available food, with increased splitting.
    Scarcity of food rationalizes straightforward movement, rebounding off walls, and cessation of reproduction.
    In extreme food scarcity, stationary existence proves optimal; non-moving fish conserve energy and outlive those expending energy in futile motion.
    Notably, strategies effective in shorter generation durations may falter when durations are extended, and vice versa.
