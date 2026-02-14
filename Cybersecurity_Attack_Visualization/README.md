# Cybersecurity Attack Visualization

Interactive 3D bubble chart visualization of network attack patterns using advanced matplotlib rendering techniques.

## Overview

This project creates a visually striking 3D bubble chart that displays network attack patterns across time and source IP addresses. The visualization uses custom matplotlib rendering to create the illusion of 3D spheres in 2D space, with color-coded attack intensities and temporal distributions.

## Features

- **3D Sphere Rendering**: Custom implementation of 3D sphere effect in 2D matplotlib
  - Layered circles with color gradients
  - Simulated shading and highlights
  - Depth perception through sizing and positioning

- **Attack Pattern Analysis**:
  - Top 10 attacking IP addresses
  - 24-hour attack distribution
  - Attack frequency visualization
  - Color-coded intensity mapping

- **Visual Design**:
  - Pastel color palette (viridis-based)
  - Professional styling and layout
  - Clear axis labels and grid
  - Optimized for presentation

## Data

**Note:** The source dataset (Honeypot_Sample_Log.csv) is not included in this repository. The notebook contains all visualizations and analysis results from the original execution.

The dataset contained:
- Honeypot attack logs
- Source IP addresses
- Timestamps (used for hourly distribution)
- Attack frequency data

## Visualization Output

The main visualization displays:
- **X-axis**: Hour of day (0-23)
- **Y-axis**: Top 10 attacking source IPs
- **Bubble size**: Attack frequency (larger = more attacks)
- **Bubble color**: Attack intensity (color-coded scale)
- **3D effect**: Custom rendering with shading and highlights

## Technical Implementation

### Custom 3D Sphere Rendering

The visualization uses a novel approach to create 3D-looking spheres:

```python
# Layered circles with decreasing opacity
# Color gradients to simulate shading
# Highlight spots for depth perception
# Size scaling based on attack count
```

### Key Technical Features:

- **Categorical data handling**: Efficient IP address categorization
- **Color mapping**: Custom pastel viridis colormap
- **Geometric calculations**: Circle positioning and sizing
- **Visual hierarchy**: Multiple layers for depth effect

## Technologies Used

- **Python 3.x**
- **Matplotlib** - Advanced 2D plotting and customization
- **Pandas** - Data manipulation
- **NumPy** - Numerical operations
- **Matplotlib Patches** - Circle rendering
- **Custom Colormaps** - Visual styling

## Use Cases

This visualization technique can be applied to:
- Network security monitoring
- Attack pattern identification
- Temporal threat analysis
- Security operations center (SOC) dashboards
- Threat intelligence reporting

## Running the Visualization

**Note:** To run this visualization, you would need honeypot log data in the expected format.

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib
   ```

2. Prepare data:
   - Place honeypot logs as `Honeypot_Sample_Log.csv` in the project directory
   - Data should include: timestamp, source_ip, and attack count columns

3. Run the notebook:
   - Open `Cybersecurity_Attack_Visualization.ipynb`
   - Run all cells to generate the visualization

## Key Insights

The visualization reveals:
- Peak attack hours (temporal patterns)
- Most active attacking IP addresses
- Attack intensity distribution
- Patterns in coordinated attacks

## Author

**Kyle Purves**

---

*This visualization demonstrates advanced matplotlib customization and creative approaches to cybersecurity data presentation.*
