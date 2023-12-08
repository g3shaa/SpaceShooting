<h1>Space Shooter Game Documentation</h1>

<h2>Introduction</h2>
<p>The Space Shooter game is an exciting arcade-style game where players control a spaceship to defeat waves of enemies.</p>

<h2>Controls</h2>
   <ul>
       <li><strong>Arrow keys:</strong> Move the spaceship (left, right, up, down).</li>
       <li><strong>Spacebar:</strong> Shoot lasers to destroy enemies.</li>
   </ul>

  <h2>Scoring</h2>
  <p>Players earn points by shooting down enemies. The game has multiple levels, and advancing to the next level requires reaching a certain point threshold.</p>

  <h2>Health and Levels</h2>
  <p>The player's spaceship has a health bar. Colliding with enemies or their lasers reduces health. Advancing through levels increases difficulty and introduces new challenges.</p>

 <h2>Installation</h2>
    <ol>
        <li>Download the game files from the repository.</li>
        <li>Ensure you have Python and Pygame installed on your system.</li>
        <li>Open a terminal and navigate to the game directory.</li>
        <li>Run the game using the command: <code>python main.py</code>.</li>
    </ol>

<h2>Building Standalone Executable</h2>
<p>If you want to share the game without requiring Python, you can build a standalone executable using PyInstaller:</p>
<code>pyinstaller --onefile --add-binary="assets;assets" main.py</code>

<h2>Troubleshooting</h2>
<p>If you encounter issues with missing assets or other problems, make sure the game's directory structure is maintained. Check the documentation or seek help from the developer community.</p>

<h2>Enjoy Playing!</h2>
<p>We hope you have a blast playing Space Shooter! For feedback or issues, please visit the official repository.</p>
