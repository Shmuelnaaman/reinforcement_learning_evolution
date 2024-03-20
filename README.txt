
# Evolution Simulator

This Evolution Simulator is an innovative Python-based project combining concepts from neural networks, genetic algorithms, and Q-learning. Agents (creatures) navigate through a maze to reach a specified goal, learning and adapting over time through a unique blend of neural network decisions and reinforcement learning strategies.

## Features

- **Neural Network-Based Decision Making:** Creatures use a simple neural network to determine their movements based on their surroundings and internal state.
- **Q-Learning with Dual Q-Tables:** Implements two distinct Q-learning algorithms, allowing creatures to learn and adapt their strategies over time.
- **Genetic Algorithms for Evolution:** Creatures can reproduce, passing on variations of their neural network weights and Q-tables to their offspring.
- **Pygame for Visualization:** Utilizes the Pygame library for rendering the maze, creatures, and their interactions in a graphical interface.

## Requirements

To run this simulation, you will need the following:

- Python 3.x
- Pygame
- NumPy

You can install the necessary Python libraries using the following command:

```bash
pip install pygame numpy tqdm
```

## Usage

To start the simulation, navigate to the directory containing the script:

Create a folder name "saved_creatures_2"

For the first run, you will need to change the value of the "new_brain_prob" in the Creature class to 1. after generating few creatures you can change that value so creatures will also b chosen from the pool of succesfull creatuers.  
 
```
class Creature:
    def __init__(self, x, y, parent_brain=None ):
        """Initialize a new Creature at coordinates (x, y) with optional parent_brain for inheritance."""
        new_brain_prob = 0.5 # change to 1 for the first run. 
```

```bash
python main.py
```

The simulation window will open, and you will see creatures navigating the maze, learning, and evolving over time.

## Structure

The code is organized into several classes:

- `Maze`: Handles the creation and rendering of the maze environment.
- `Brain`: Manages the decision-making logic, including the neural network and Q-learning algorithms.
- `Creature`: Represents an agent within the environment, containing its logic for sensing, decision-making, and movement.
- `PopulationManager`: Manages the population of creatures, including spawning, updating, and reproducing agents.
- `Main`: Sets up the simulation and manages the main game loop.

## Customization

You can customize various aspects of the simulation, including the maze layout, creature attributes, and learning parameters, by modifying the respective class properties and methods.

## Contributing

Contributions to the Evolution Simulator are welcome! If you have suggestions for improvements or new features, feel free to create an issue or submit a pull request.

## License

This project is open source and available under the [MIT License](LICENSE).

---