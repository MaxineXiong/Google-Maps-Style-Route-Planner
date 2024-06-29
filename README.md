# Google Maps Style Route Planner with A* Search Algorithm

[![GitHub](https://badgen.net/badge/icon/GitHub?icon=github&color=black&label)](https://github.com/MaxineXiong)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with Python](https://img.shields.io/badge/Python->=3.6-blue?logo=python&logoColor=white)](https://www.python.org)

<br/>

This project is an implementation of a route planning algorithm inspired by ***Google Maps***. It utilizes the **A\* search algorithm** to find the shortest path between two points on a given map. The algorithm considers both the actual path cost and an estimated distance to the destination using the Euclidean distance formula. With this route planner algorithm, users can effectively plan routes on various maps, finding the most efficient path between their desired locations.

<br/>

## Features

- Create and plot maps with intersections and roads.
- Calculate the shortest path and distance between two points on a map.
- Perform tests on maps of different complexity to verify the correctness of the algorithm.

<br/>

## **Repository Structure**

This repository follows the following directory structure:

```
Google-Maps-Style-Route-Planner
├── Google_Maps_Style_Route_Planner.ipynb
├── maps.py
├── README.md
└── LICENSE
```

- **Google_Maps_Style_Route_Planner.ipynb**: This Jupyter Notebook serves as the primary file for the project. It contains the major functions responsible for displaying the map and calculating the shortest path. Users can import all the necessary functions from this notebook for their own use.
- **maps.py**: This file stores the map data and is imported into the **Google_Maps_Style_Route_Planner.ipynb** notebook. It provides the underlying data structure and utilities required for map manipulation and path finding.
- **README.md**: Provides an overview of this repository.
- **LICENSE**: The license file for the project.

Please note that the **Google_Maps_Style_Route_Planner.ipynb** notebook should be used as the main entry point for interacting with the project.

<br/>

## Prerequisites

- Python (version 3.6 or higher)
- Jupyter Notebook
- Matplotlib (for map visualization)
- ipynb (for notebook integration)

<br/>

## Installation

1. Clone the repository:

```
git clone https://github.com/your_username/route-planner.git
```

2. Install the required dependencies:

```
pip install matplotlib
pip install ipynb
```

<br/>

## **Usage**

To integrate the algorithm into your own project, please ensure that your map data has been transformed into the same format as **`maps.py`**. Then, follow the steps below:

1. Import all functions from **Google_Maps_Style_Route_Planner.ipynb**:
    
    ```python
    from ipynb.fs.defs.Google_Maps_Style_Route_Planner import *
    ```
    
2. Create a map using the **`create_map`** function:
    
    ```python
    your_map = create_map([your_X_LINES], [your_Y_LINES], 
                          [your_X_SCATTERS], [your_Y_SCATTERS],
                          [your_MARKERS])
    ```
    
3. (Optional) Plot the base map using the **`plot_map`** function:
    
    ```python
    plot_map([your_X_LINES], [your_Y_LINES],
             [your_X_SCATTERS], [your_Y_SCATTERS],
             [your_MARKERS])
    plt.show()
    ```
    
4. Calculate the shortest path and distance between two intersections using the **`compute_shortest_path`** function:
    
    ```python
    shortest_path, shortest_distance = compute_shortest_path(
        map=your_map, start=[your_start_id], goal=[your_goal_id]
    )
    ```
    
5. (Optional) Verify the algorithm's correctness and visualize the highlighted shortest path on the map by running the **`test`** function:
    
    ```python
    test(
        map=your_map,
        start=[your_start_id],
        goal=[your_goal_id], 
        actual_shortest_path=[your_actual_shortest_path], 
        x_lines=[your_X_LINES],
        y_lines=[your_Y_LINES],
        x_scatters=[your_X_SCATTERS],
        y_scatters=[your_Y_SCATTERS], 
        markers=[your_MARKERS],
        show_plot=True,
    )
    ```

    <br/>

    <p align='center'>
      <img src="https://github.com/MaxineXiong/Google-Maps-Style-Route-Planner/assets/55864839/22b0df53-7ddf-48e4-8651-2a75423eb52a" width = "800">
      <br><i>Example output of the `test` function</i>
    </p>
    
<br/>

## **Contributing**

Contributions are welcome! If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request. Make sure to follow the **[code of conduct](https://docs.github.com/en/site-policy/github-terms/github-community-code-of-conduct)**.

<br/>

## **License**

This project is licensed under the **[MIT License](https://choosealicense.com/licenses/mit/)**.
