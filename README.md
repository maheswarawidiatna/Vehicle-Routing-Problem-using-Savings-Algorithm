# Vehicle Routing Problem using Savings Algorithm

## Overview

This script solves the Vehicle Routing Problem (VRP) using the Savings Algorithm. The VRP involves optimizing the routes of a fleet of vehicles to deliver goods to a set of locations while minimizing total transportation costs.

## Script Contents

### 1. Dependencies

- **numpy**: For numerical operations.
- **pandas**: For data manipulation and analysis.
- **matplotlib.pyplot**: For data visualization.
- **google.colab**: For interaction with Google Colab environment.

### 2. Functions

#### 2.1 VRP Savings Algorithm Function

- **do_savings_algo(distance, demand, capacity, *nodes, display=False, dictate=False):**
  - Solves VRP using the Savings Algorithm.
  - Inputs:
    - `distance`: Distance matrix between locations.
    - `demand`: Demand for each location.
    - `capacity`: Vehicle capacity.
    - `*nodes`: Coordinates of locations (optional).
    - `display`: Whether to display the routes (optional).
    - `dictate`: Whether to print the route details (optional).
  - Outputs:
    - Returns a list of routes for each vehicle.

#### 2.2 Data Generation Functions

- **gen_distance_arr(n, min=-100, max=100, display=False):**
  - Generates random location coordinates and computes the distance matrix.
  - Inputs:
    - `n`: Number of locations.
    - `min`: Minimum coordinate value (optional).
    - `max`: Maximum coordinate value (optional).
    - `display`: Whether to display the generated locations (optional).
  - Outputs:
    - Returns distance matrix and location coordinates.

- **gen_demand_arr(n, min=10, max=100):**
  - Generates random demand values for each location.
  - Inputs:
    - `n`: Number of locations.
    - `min`: Minimum demand value (optional).
    - `max`: Maximum demand value (optional).
  - Outputs:
    - Returns an array of demand values.

#### 2.3 Data Processing Function

- **prc_data_xlsx(display=False):**
  - Processes data from an uploaded Excel file.
  - Inputs:
    - `display`: Whether to display the locations (optional).
  - Outputs:
    - Returns location coordinates, distance matrix, demand array, and location descriptions.

### 3. Demo (Fabricated Data)

1. Set parameters: `point` (number of locations) and `capacity` (vehicle capacity).
2. Generate data using `gen_distance_arr` and `gen_demand_arr`.
3. Compute routes using `do_savings_algo` and display the results.

### 4. Usage (Real Data)

1. Set parameters: `capacity` (vehicle capacity).
2. Upload, fill, and input data using the provided template or example format.
3. Compute routes using `do_savings_algo` and display the results.

## 5. Result

**Fabricated Data:**

Before

![download (3)](https://github.com/maheswarawidiatna/Vehicle-Routing-Problem-using-Savings-Algorithm/assets/94330691/c7ba8445-64c3-47d5-9ab4-57b6a60f9fc3)

After

![download (1)](https://github.com/maheswarawidiatna/Vehicle-Routing-Problem-using-Savings-Algorithm/assets/94330691/bbb145e0-66d3-4583-852e-4fbd27ecff19)

**Real Data:**

Before

![download (4)](https://github.com/maheswarawidiatna/Vehicle-Routing-Problem-using-Savings-Algorithm/assets/94330691/1bda261f-900d-4e8f-9b6d-61d9a0125efd)

After

![download (2)](https://github.com/maheswarawidiatna/Vehicle-Routing-Problem-using-Savings-Algorithm/assets/94330691/a473493d-ee28-4402-8eb9-f5b40b2edd7c)

## Example

```python
# Set parameters
point = 50
capacity = 1000

# Generate data
distance, coordinate = gen_distance_arr(point, display=True)
demand = gen_demand_arr(point)

# Compute routes using Savings Algorithm
plan = do_savings_algo(distance, demand, capacity, coordinate, display=True, dictate=True)
```

For a real-world example, upload an Excel file using `prc_data_xlsx` and follow the same steps.

**Note:** Ensure that the uploaded file contains columns 'x', 'y', 'demand', and 'description' for processing.

Feel free to modify the script according to your specific requirements.
