# Reinforcement-Learning
## Disaster Management: Safe Evacuation Routes

### Overview

This project implements a system to determine safe evacuation routes in a city during a disaster. The system uses a combination of Dijkstra's algorithm to find the shortest path and Q-learning (a reinforcement learning technique) to adapt routes based on user feedback. The goal is to not only find the shortest path but also adaptively learn safer routes as users provide feedback about the safety of different paths.

### How It Works

1. **City Map Simulation:**
   - The city is represented as a 10x10 grid where intersections are nodes, and roads between intersections are edges with weights (representing road conditions such as travel time or safety).
   - Disaster zones are simulated by increasing the weights of edges connected to certain nodes, representing dangerous areas.

2. **Dijkstra's Algorithm:**
   - Initially, Dijkstra's algorithm is used to find the shortest path from a start node to a destination node. This path is based solely on the static weights of the edges (e.g., distance or travel time).

3. **Q-Learning with User Feedback:**
   - Q-learning is then applied to learn safer routes over time by incorporating user feedback. The feedback is simulated in this code for demonstration purposes.
   - The Q-learning algorithm adapts the route recommendations by updating Q-values for actions (moving from one node to another) based on the rewards (positive or negative feedback).
   - If a user indicates a path is unsafe, the corresponding Q-values are penalized, encouraging the system to avoid such paths in the future.

4. **Visualization:**
   - The code visualizes the initial road network and the paths identified by both Dijkstra’s algorithm and Q-learning.
   - After running Q-learning, the system shows how the optimal path evolves based on the feedback received.

### Key Components

- **Dijkstra's Algorithm:** Used to calculate the shortest path in the static city map.
- **Q-Learning Algorithm:** Reinforcement learning technique that allows the system to adapt the path suggestions based on feedback.
- **User Feedback Simulation:** For demonstration, feedback is randomly generated, but it can be integrated with real user inputs in a production environment.

### How to Use

1. **Dataset Creation:** The city map and disaster zones are generated using simulated data.
2. **Run Dijkstra's Algorithm:** Calculates and visualizes the shortest path based on the initial conditions.
3. **Apply Q-Learning:** Simulates feedback and updates the path recommendations accordingly.
4. **Visualize Results:** Compares the paths identified by Dijkstra’s algorithm and the Q-learning approach.

### Future Improvements

- **Real Data Integration:** Replace simulated data with real-world data on city maps and disaster zones.
- **Dynamic User Feedback:** Implement a system to gather real-time feedback from users about the safety of different routes.
- **Scalability:** Expand the grid size or integrate real geographic data to make the system applicable to larger cities or regions.

### Conclusion

This code provides a basic framework for developing a disaster management system that adapts evacuation routes based on real-time feedback, making it a valuable tool for enhancing public safety during emergencies.

