Purpose
This project is a Java-based GUI application designed to simulate an underwater cave diving experience. The program uses basic user interface components and a recursive algorithm to help a diver find an escape route through a randomly generated underwater cave.

Overview
The Cave Diver program displays a 10x10 grid representing an underwater cave, where each cell has a unique depth and color based on the depth. The diver, starting from the upper-left corner, must navigate through the cave with limited air supply and find an escape route to the lower-right corner. The GUI, implemented using Java Swing and AWT, provides interactive features and visual cues to guide the user in this adventure.

Features
    Randomly Generated Cave: Each cell's depth is randomly assigned and displayed as a blue rectangle, with shades indicating depth (lighter for shallow, darker for deeper).
    Escape Route: The diver starts with 20 units of air, losing 1 unit per move. The goal is to find a safe path to the exit without exceeding the depth rating or running out of air.
    User Interaction:
        Enter a depth rating for the diver.
        Click "Escape" to find a route.
        "New Cave" generates a new random cave layout.
    Recursive Pathfinding: The application uses a recursive algorithm to determine if an escape route exists.
        If successful, the escape route is marked in red.
        If no route is possible, a message is displayed.

Instructions
    Set Depth Rating: Enter a depth rating in the input field.
    Find Escape Route: Press "Escape" to see if the diver can exit based on the rating.
    Generate New Cave: Use "New Cave" to reset with a new random layout.

Technical Details
    Grid Layout: The main cave area is a 10x10 grid, with each cell represented by a CaveCell object.
    Depth and Color: Cells are colored based on depth using java.awt.Graphics. Shallow cells appear lighter, while deeper cells are darker.
    Recursive Escape Algorithm: A recursive method attempts to find a path by moving only downward or to the right. If a solution is found, the path is marked in red as the recursion unwinds.

GUI Design
    Top Label: Displays title and instructions.
    Center Cave Display: A JComponent shows the cave grid.
    Bottom Controls: Includes a label, input field for depth rating, and buttons for "Escape" and "New Cave".
