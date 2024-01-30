# Introduction
  Flappy Bird AI, is a project that combines the iconic Flappy Bird game with artificial intelligence to enable autonomous learning. In this repository, you'll find a fully functional Flappy Bird game implemented in Python with an AI system that 
  trains itself to play the game and evolves and improves over time.

# Algorithm
  The Flappy Bird AI employs the NEAT algorithm to evolve neural networks that control the behavior of the Flappy Bird to maximize its performance. 
  NEAT is a neuroevolutionary algorithm that combines the principles of genetic algorithms and neural networks to evolve increasingly sophisticated neural network structures over generations.

# Key-Components of NEAT

  * DefaultGenome for node activation, node aggregation, node bias, genome compatibility, connection rates, and feed-forward.

  * DefaultSpeciesSet for compatibility threshold.

  * DefaultStagnation for fitness function and elitism.

  * DefaultReproduction for calculating survival.

# Classes:
  * Bird:
    * Represents the player-controlled bird character.
    
    * Handles bird movement, jumping, animation, and drawing.
    
    * Implements pixel-perfect collision detection using get_mask() method.

  * Pipe:

    * Represents the pipes that the bird must navigate through.

    * Manages pipe movement, drawing, and collision detection with the bird.
      
  * Base:

    * Represents the base of the game where the bird stands.

    * Handles base movement and drawing.

# Functions:

  * draw_window:

    * Draws the game window with the background, pipes, base, score, and birds.

    * Updates the display.

  * main:

    * The main game loop that initializes the game elements.

    * Manages the NEAT algorithm by evaluating the neural networks based on bird behavior.

    * Handles user input events (such as quitting the game).

    * Manages bird and pipe movement, collision detection, and updating the game state.

    * Uses the Pygame clock to control the frame rate.

# NEAT Integration:

  * The main function initializes neural networks for each bird using the NEAT algorithm.

  * The neural networks are used to determine the bird's actions based on input parameters such as the bird's Y-coordinate, the vertical distance to the pipes, and the horizontal distance to the next pipe.

  * The NEAT genomes (`ge`) are used to track the fitness of each bird, rewarding or penalizing based on their performance.

  * The game continues until all birds are eliminated or the user quits.

# Pygame Integration:

  * Pygame is used for window initialization, handling events, and drawing graphics.

  * Images for the bird, pipes, background, and base are loaded and scaled using Pygame functions.

  * The game window is updated in the draw_window function.
