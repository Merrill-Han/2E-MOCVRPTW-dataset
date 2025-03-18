# E-MOCVRPTW Simulation Dataset

## **1. Overview**
This dataset provides benchmark instances for the **Multi-Objective Capacitated Vehicle Routing Problem with Time Windows (E-MOCVRPTW)**. The instances are designed based on real-world logistics data from **Futian District, Shenzhen, China**, and simulate a **two-tier logistics network** within a **10×10 plane region**.

The dataset consists of:
- **Three suppliers, seven retail stores, and 140 customers.**
- **Customer demand scenarios** categorized by spatial distribution.
- **Two-stage problem instances** reflecting the two-tier logistics structure.

This dataset can be used for research in **vehicle routing optimization, last-mile delivery planning, and collaborative logistics networks**.

---

## **2. Naming Conventions**
Each instance follows the naming format:E-x,y-z-n

where:
- **x, y**: Represent the distribution of **first-tier nodes (suppliers) and second-tier nodes (retailers)**.
- **z**: Represents the clustering degree of customer distribution.
- **n**: Represents the instance number for a particular distribution pattern.

### **Customer Distribution Scenarios (`z` value)**
- **c**: Clustered (High-density customer zones)
- **u**: Uniform (Evenly spread customers)
- **d**: Dispersed (Scattered customer locations)

### **Logistics Node Distribution Scenarios (`x, y` values)**
| Scenario | Suppliers (`x`) | Retailers (`y`) | Description |
|----------|--------------|----------------|-------------|
| **E-4,3-u-n** | 4 | 3 | Supplier nodes in urban centers, retailers in commercial areas (e.g., Futian CBD) |
| **E-4,2-u-n** | 4 | 2 | Suppliers in commercial hubs, retailers closer to customer zones |
| **E-3,4-u-n** | 3 | 4 | Suppliers near city center, retailers spread in suburban areas |

---

## **3. Data Format**
Each instance is stored as two `.txt` files:
1. **First-stage file (`E-x,y-z-n-1st.txt`)** - Supplier to Retailer assignment.
2. **Second-stage file (`E-x,y-z-n-2rd.txt`)** - Retailer to Customer assignment.

Each file consists of **9 columns**:

| Column | Description |
|--------|-------------|
| `1` | Index (Customer ID) |
| `2` | X coordinate |
| `3` | Y coordinate |
| `4` | Demand quantity (q) |
| `5` | Assigned enterprise (1-n) |
| `6` | Participation in collaboration (1: Yes, 0: No) |
| `7` | Earliest service time |
| `8` | Latest service time |
| `9` | Service duration |

## **4. Code for Instance Generation**
This dataset is accompanied by two scripts for instance generation:

### **1. MATLAB Code: Three-Level Node Generation**
- **File:** `Three-level node generation code.txt`
- **Description:** MATLAB script for simulating **supplier-retailer-customer** hierarchical node distributions.
- **Usage:** Run the script in MATLAB to generate random instances.

### **2. Python Code: Customer Point Attribution**
- **File:** `Customer point attribution code.txt`
- **Description:** Python script for assigning customer points to retailers and suppliers.
- **Usage:** Run the script with the input dataset to classify customers based on demand and spatial proximity.

# Shenzhen Futian VRP Dataset
## Overview
This dataset provides real-world benchmark instances for the **Vehicle Routing Problem (VRP)** collected from **Shenzhen Futian District, China**. The dataset includes **customer locations, demand values, time window constraints, and hierarchical supply relationships** between customers, retailers, and suppliers. It is useful for research on:
- **Vehicle Routing Problem with Time Windows (VRPTW)**
- **Last-mile delivery optimization**
- **Retailer-supplier network analysis**
- **Geospatial logistics optimization**

## Data Structure
The dataset is stored in the file **`VRP_Shenzhen_Futian.csv`** within the `datasets/` directory.

### **File Format**
- **Format:** CSV (Comma-Separated Values)
- **Encoding:** UTF-8
- **Delimiter:** Comma `,`

### **Column Descriptions**
| Column Name              | Description |
|--------------------------|-------------|
| `No.`                   | Unique customer ID |
| `Latitude`              | Customer location (Latitude) |
| `Longitude`             | Customer location (Longitude) |
| `x`                     | Projected coordinate (X-axis from ArcGIS) |
| `y`                     | Projected coordinate (Y-axis from ArcGIS) |
| `Demand`                | Customer demand quantity |
| `Nature of coordinates` | Identifier for customer coordinates (e.g., A1-1) |
| `Belong-1st`            | Retailer ID associated with the customer |
| `Belong-2rd`            | Supplier ID associated with the retailer |
| `Start time`            | Time window start (in minutes) |
| `End time`              | Time window end (in minutes) |
| `Service time`          | Required service duration at the customer location (in minutes) |

