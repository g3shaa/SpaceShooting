<h1>Space Shooter Game Documentation</h1>

<h2>Introduction</h2>
<p>The Space Shooter game is a classic arcade-style game developed using Pygame. Players control a spaceship,
    battling through waves of enemy ships and shooting lasers to survive and score points.</p>

<h2>Game Assets</h2>
<p>The game utilizes various images for spaceships, lasers, and backgrounds. These images are loaded into the game
    using Pygame's <code>pygame.image.load</code> method. The assets include:</p>
<ul>
    <li>Red, green, blue, and yellow spaceships</li>
    <li>Laser images corresponding to different colors</li>
    <li>Background image</li>
</ul>

<h2>Classes and Functions</h2>

<h3>Laser Class</h3>
<p>The <code>Laser</code> class represents the projectiles fired by spaceships. It has the following methods:</p>
<ul>
    <li><code>__init__(self, x, y, img)</code>: Initializes a laser object with given coordinates and an image.</li>
    <li><code>draw(self, window)</code>: Draws the laser on the game window.</li>
    <li><code>move(self, vel)</code>: Moves the laser vertically based on the provided velocity.</li>
    <li><code>off_screen(self, height)</code>: Checks if the laser is off the screen.</li>
    <li><code>collision(self, obj)</code>: Checks for collision between the laser and another game object.</li>
</ul>

<h3>Ship Class</h3>
<p>The <code>Ship</code> class is the base class for both the player's spaceship and enemy spaceships. It includes:
</p>
<ul>
    <li><code>__init__(self, x, y, health=100)</code>: Initializes a ship object with coordinates and health.</li>
    <li><code>draw(self, window)</code>: Draws the ship and its lasers on the game window.</li>
    <li><code>move_lasers(self, vel, obj)</code>: Moves the ship's lasers and handles collisions with other objects.
    </li>
    <li><code>cooldown(self)</code>: Manages the cooldown time between shots.</li>
    <li><code>shoot(self)</code>: Fires a laser from the ship.</li>
    <li><code>get_width(self)</code>: Returns the width of the ship.</li>
    <li><code>get_height(self)</code>: Returns the height of the ship.</li>
</ul>

<h3>Player Class</h3>
<p>The <code>Player</code> class inherits from the <code>Ship</code> class and represents the player-controlled
    spaceship. Additional functionalities include:</p>
<ul>
    <li><code>__init__(self, x, y, health=100)</code>: Initializes a player object with initial health, images, and
        score-related attributes.</li>
    <li><code>move_lasers(self, vel, objs)</code>: Extends the base class to handle collisions and scoring points.
    </li>
    <li><code>healthbar(self, window)</code>: Draws the player's health bar on the game window.</li>
    <li><code>display_stats(self, window)</code>: Displays the player's points and level information on the game
        window.</li>
</ul>

<h3>Enemy Class</h3>
<p>The <code>Enemy</code> class inherits from the <code>Ship</code> class and represents the enemy spaceships. It
    includes:</p>
<ul>
    <li><code>__init__(self, x, y, color, health=100)</code>: Initializes an enemy object with coordinates, color,
        and health.</li>
    <li><code>move(self, vel)</code>: Moves the enemy spaceship vertically based on the provided velocity.</li>
    <li><code>shoot(self)</code>: Fires a laser from the enemy spaceship.</li>
</ul>

<h2>Game Flow</h2>
<p>The game progresses through levels as the player scores points by shooting down enemy spaceships. Each level
    increases in difficulty, with more enemies and faster movement. The player loses health when hit by enemy lasers
    or when an enemy spaceship successfully passes the player.</p>

<h2>Menus</h2>
<p>The game includes main and game-over menus:</p>
<ul>
    <li><code>main_menu()</code>: Displays the main menu with the game title and instructions. Players can start the
        game by pressing the SPACE key.</li>
    <li><code>game_over_menu()</code>: Displays the game-over menu when the player loses. It shows the "You Lost!!"
        message, play again button, close game button, and player's points and level information.</li>
</ul>

<h2>Main Functionality</h2>
<p>The <code>main()</code> function is the core of the game. It handles the game loop, player input, enemy movement,
    collisions, and other game-related logic.</p>
