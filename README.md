# README

## Player Movement System

A simple object-oriented Python implementation of a character movement system using abstract base classes and inheritance.

### Overview

This project demonstrates basic game mechanics where a player character (Pawn) can move on a 2D grid. The system uses:

- Abstract base classes to define the `Player` interface
- Inheritance to create specific character types
- Random movement selection from predefined move sets
- Path tracking of all positions visited

### Classes

#### `Player` (Abstract Base Class)
- **Attributes:**
  - `moves`: List of possible movement vectors
  - `position`: Current (x, y) coordinates
  - `path`: List of all visited positions
- **Methods:**
  - `make_move()`: Randomly selects and executes a move, updates position and path
  - `level_up()`: Abstract method to be implemented by subclasses

#### `Pawn` (Inherits from Player)
- **Initial moves:** Four-directional movement (up, down, left, right)
  - `(0, 1)` - Up
  - `(0, -1)` - Down
  - `(1, 0)` - Right
  - `(-1, 0)` - Left
- **Level up:** Extends moves to include diagonal movement
  - `(1, 1)`, `(-1, 1)`, `(-1, -1)`, `(1, -1)`

### Usage

```python
# Create a pawn character
character = Pawn()

# Make a random move
new_position = character.make_move()
print(new_position)  # Output: (x, y) coordinates
```

### Example Output

```
(1, 0)  # Random move to the right
```

### Potential Enhancements

- Add more character types (Knight, Bishop, Rook, Queen)
- Implement validation to prevent moves that go out of bounds
- Add level progression system
- Create a game board visualization
- Add movement history with timestamps
- Implement deterministic movement strategies

### Requirements

- Python 3.x
- No external dependencies required

### Running the Code

Simply execute the main.py file:

```bash
python main.py
```
