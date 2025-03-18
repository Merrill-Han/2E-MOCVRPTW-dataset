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

