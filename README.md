# AI-simulated-Flappy-birds-game-NEAT-


https://github.com/user-attachments/assets/2bf13a3b-5be7-4a46-957b-60b0641be023



https://github.com/user-attachments/assets/9b56e50b-a13d-45a2-9e44-3948899106d8



---

# Flappy Bird AI Simulation

This project uses the NEAT (NeuroEvolution of Augmenting Topologies) algorithm to train a neural network to play the game **Flappy Bird**. The AI controls multiple bird agents and learns to navigate through pipes by simulating evolution over generations.

## Features

- **Pygame-Based Simulation**: The game and environment are built using the `Pygame` library.
- **Neural Network**: NEAT is used to evolve neural networks, allowing the birds to learn the game.
- **Real-time Visualization**: You can watch the AI improve its gameplay as the generations progress.
- **Configurable Parameters**: NEAT's hyperparameters are easily adjustable using a configuration file.

## Requirements

Before you can run the project, ensure you have the following installed:

- Python 3.7+
- Pygame (`pip install pygame`)
- Neat-Python (`pip install neat-python`)

## How to Run

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/your-username/FlappyBird-AI.git
   cd FlappyBird-AI
   ```

2. **Set Up the Environment**:

   Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Simulation**:

   Run the following command to start the AI training:

   ```bash
   python cae.py
   ```

4. **NEAT Configurations**:

   The NEAT algorithm is configured using the `config-feedforward.txt` file. You can tweak this file to adjust parameters like population size, mutation rates, and more.

## File Structure

```
├── imgs/                   # Game assets (bird, pipes, background)
├── cae.py                  # Main game and AI script
├── config-feedforward.txt   # NEAT configuration file
├── README.md               # Project documentation
├── visualize.py            # NEAT visualization utilities
```

## Key Classes

- **Bird**: Represents the bird controlled by the AI, with methods for movement, jumping, and drawing.
- **Pipe**: Represents the pipes in the game. The AI must avoid colliding with these.
- **Base**: Represents the moving floor in the game.
- **NEAT**: A genetic algorithm framework used to evolve the birds' neural networks to play Flappy Bird.

## How the AI Works

The AI uses a neural network to control the birds. Inputs to the neural network include:

- The bird's vertical distance from the next pipe.
- The height of the next pipe.
- The bottom of the next pipe.

The output from the neural network determines whether or not the bird will jump.

The NEAT algorithm evolves the neural networks over many generations, selecting the best-performing birds and mutating their networks to improve performance.

## Example Gameplay

The AI will start with very little knowledge and will often crash early on. However, as generations progress, the AI will learn to navigate through the pipes and survive for longer periods.

## Customization

- **Tuning NEAT**: Modify the `config-feedforward.txt` to tune the genetic algorithm parameters like population size, mutation rates, and more.
- **Game Speed**: Adjust the frame rate to speed up or slow down the game for faster or slower learning.

## Credits

- This project uses the [NEAT-Python](https://neat-python.readthedocs.io/en/latest/) library for implementing the NEAT algorithm.
- Pygame is used for the game simulation and rendering.

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).

---

This `README.md` file gives a clear overview of the project, instructions for running it, and some background on how the AI works. Adjust any project-specific information, such as the repository URL and other details, before uploading to GitHub.
