
 Shortest Path Visualiser
An interactive, web-based tool for visualizing classic shortest path algorithms on real-world road networks. Powered by live data from OpenStreetMap (OSM) and built with Vanilla JavaScript and Leaflet.js.

✨ Core Features
🌍 Live OSM Data Integration: Dynamically fetches and renders road networks (highways) for any location worldwide using the Overpass API.

🔗 On-the-Fly Graph Generation: Instantly converts raw geographic data from OSM into a functional graph structure (nodes and adjacency lists) ready for pathfinding.

🧮 Multiple Algorithm Support:

Dijkstra’s Algorithm: The classic, guaranteeing the shortest path on networks with non-negative edge weights.

A* Search: A powerful heuristic-based algorithm that intelligently finds the shortest path much faster than Dijkstra's in most real-world scenarios.

Bellman-Ford Algorithm: Capable of handling negative edge weights, included for academic and demonstration purposes.

🖱 Intuitive Map Interface: Simply click on the map to define your start and end points. The application automatically snaps to the nearest valid road intersection.

💻 Zero-Dependency Codebase: The entire application is contained within a single HTML file. No build tools, no frameworks, no complex setup—just open index.html and go. It's incredibly easy to read, modify, and extend.

🚀 Getting Started
Getting the visualiser running is simple.

Clone the Repository

Bash

git clone https://github.com/shivam02345/shortest_path.git
cd shortest_path
Open in Browser
Open the index.html file in any modern web browser like Chrome, Firefox, or Edge.

Find a Path
🗺️ Pan and zoom to your desired area.
📥 Click "Load graph around map center" to fetch the local road data.
📍 Set your Start and End points with two clicks on the map.
⚡ Choose an algorithm from the dropdown and click "Find Path".
✅ The optimal route will be drawn on the map, with distance and time metrics displayed in the log.

🛠️ Implementation Details
Graph Model: The road network is modeled as a graph where nodes are OSM IDs with associated coordinates. The graph is stored in an adjacency list for efficient traversal.

Edge Weights: Edge weights represent real-world distances (in meters) between two nodes, calculated precisely using the Haversine formula.

Priority Queue: A custom-built MinHeap data structure is used to ensure efficient implementation of Dijkstra’s and A* algorithms.

Data Sourcing: The Overpass API is queried to retrieve all highway elements within the current map's bounding box.

UI & Rendering: The entire user interface and map rendering are handled with lightweight HTML, CSS, and Leaflet.js.

📜 Algorithms Explained
🔹 Dijkstra: A foundational algorithm that explores nodes in order of increasing distance from the source. It is guaranteed to find the absolute shortest path.

🔹 A*: An optimized version of Dijkstra that uses a heuristic (Euclidean distance to the target) to guide its search, significantly reducing computation time by exploring in the right direction.

🔹 Bellman-Ford: A more robust algorithm that can handle graphs with negative edge weights, though it is slower (O(VE)) than the alternatives.
