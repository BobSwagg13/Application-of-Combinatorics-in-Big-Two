# README: Capsa Simulation

## Overview
This project provides a Python-based simulation and analysis of the card game Capsa using object-oriented programming and Monte Carlo methods. The primary components are a deck of cards, player logic for determining various hand combinations, and statistical simulations for probability analysis.

## Files

### 1. `capsa.py`
This file defines the core classes and logic for the Capsa simulation.

#### Classes

1. **Card**: Represents an individual playing card.
   - Attributes: `value`, `suit`
   - Methods: `__str__()` for string representation.

2. **Deck**: Represents a standard 52-card deck.
   - Methods:
     - `create_deck()`: Initializes the deck.
     - `get_random_cards(n)`: Returns `n` random cards from the deck.

3. **Player**: Represents a player with hand management and combination detection.
   - Methods:
     - `receive_cards(cards)`: Adds cards to the player’s hand.
     - `reset_hand()`: Resets the hand to empty.
     - Combination detection:
       - `exist_pair()`
       - `exist_three_of_a_kind()`
       - `exist_straight()`
       - `exist_flush()`
       - `exist_full_house()`
       - `exist_four_of_a_kind()`
       - `exist_straight_flush()`
     - Combination generation and counting:
       - `pair_combinations()`
       - `three_of_a_kind_combinations()`
       - `straight_combinations()`
       - `flush_combinations()`
       - `full_house_combinations()`
       - `four_of_a_kind_combinations()`
       - `straight_flush_combinations()`
     - Statistical counts for combinations (e.g., `number_of_combinations_pair()`).

#### Main Function
The `main()` function demonstrates the functionality by:
- Generating a random hand of 13 cards.
- Checking for various hand combinations.
- Printing combination statistics and examples.

### 2. `monte_carlo.py`
This file performs a Monte Carlo simulation to calculate the probabilities of various hand combinations.

#### Workflow
1. Imports the `Deck` and `Player` classes from `capsa.py`.
2. Simulates `n` rounds (default 1,000,000).
3. In each round:
   - A player receives a random hand of 13 cards.
   - Checks for the existence of each combination.
   - Resets the hand for the next round.
4. Outputs the probabilities of each combination type.

#### Output Example
```
Pair:  99.9908 %
Three of a kind:  49.0509 %
Straight:  59.5018 %
Flush:  62.2549 %
Full house:  49.0509 %
Four of a kind:  3.4273 %
Straight flush:  0.1146 %
```

## How to Run

### Prerequisites
- Python 3.12.6

### Running the Simulation
1. Clone the repository.
2. Run the combination checker:
   ```bash
   python capsa.py
   ```
3. Run the Monte Carlo simulation:
   ```bash
   python monte_carlo.py
   ```

## Project Features
- **Deck Management**: Creation and shuffling of a 52-card deck.
- **Combination Detection**: Identification of pairs, straights, flushes, and other Capsa hand combinations.
- **Statistical Analysis**: Monte Carlo simulation to compute probabilities.
- **Extensible Design**: Classes and methods can be easily extended for additional features or games.

## Future Improvements
- Add support for additional hand combinations or rules specific to variations of Capsa.
- Optimize combination detection algorithms for efficiency.
- Provide a graphical user interface (GUI) for better usability.
- Implementation for AI

## Author
Bob Kunanda
13523086


