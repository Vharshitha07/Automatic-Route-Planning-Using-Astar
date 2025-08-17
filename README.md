🚗 Andhra Pradesh Route Optimizer using A* Search with Traffic and Blockage Awareness
This project implements an intelligent route optimization system using the A* search algorithm to find the fastest path between two cities in Andhra Pradesh, India. It factors in real-time traffic conditions, road blockages, and geographical coordinates to estimate the optimal travel time and path.

📌 Features
✅ A* Search Algorithm tailored for travel time as the cost.

🚦 Traffic Multipliers to simulate real-world congestion.

🚧 Blocked Roads Handling to avoid unavailable routes.

🧭 Heuristic-based Estimations using straight-line distances to the destination.

🗺️ Interactive Map Visualization with Folium, showing:

All roads (normal, traffic-affected, and blocked)

The optimal path in green

City-wise tooltips for better understanding

🧠 Technologies Used
Python 3.x

folium – For map rendering

heapq – For priority queue implementation of A* algorithm

geopy (optional, for geographical calculations if extended)

🚀 How It Works
Cities & Distances: Defined in a graph with direct roads and their respective distances.

Traffic Factors: Simulated multipliers to slow down travel on busy routes.

Blocked Roads: Routes that are unavailable are excluded from the search.

Heuristic: Straight-line distance from each city to the destination (Hyderabad) is used to guide A*.

A* Search: Finds the optimal path from Tirupati to Visakhapatnam using both actual and heuristic travel time.

Map: An interactive map is generated with:

Red dashed lines: Blocked roads

Gray lines: All roads with traffic weights

Green lines: The optimal route

📂 Project Structure
bash
Copy
Edit
├── route_optimizer.py               # Main Python script
├── andhra_pradesh_time_a_star_full_overrides.html  # Output map file
├── README.md                        # This file
🔧 Installation
Install required packages:

bash
Copy
Edit
pip install folium geopy
Then run the script:

bash
Copy
Edit
python route_optimizer.py
📊 Output
Console Output: Displays the optimal path, total estimated time, and segment-wise details.

HTML Map: Opens a beautiful interactive map showing the cities, routes, and optimal path.

📝 Example Output
plaintext
Copy
Edit
Optimal path: Tirupati → Ongole → Vijayawada → Guntur → Rajahmundry → Anakapalli → Visakhapatnam
Total estimated travel time: 11.36 h

Segment details:
  Tirupati → Ongole: 175 km, traffic ×1.03, ≈ 3.00 h
  ...
Map saved to andhra_pradesh_time_a_star_full_overrides.html
🌍 Map Preview (open in browser)
📍 andhra_pradesh_time_a_star_full_overrides.html

Includes markers, traffic indicators, and the green-highlighted optimal path.

![image](https://github.com/user-attachments/assets/9e6b646b-b255-4797-979b-f2613563d708)


🧠 Possible Enhancements
Integrate real-time traffic data using APIs like Google Maps or OpenStreetMap.

Add user input to dynamically choose start and end cities.

Incorporate fuel cost or toll information for multi-factor optimization.

Extend the map to include Telangana or pan-India routes.

🙌 Acknowledgements
Folium for the beautiful mapping tool.

Dijkstra & A* for foundational search algorithms.

Geolocation data inspired by real coordinates from Google Maps.
