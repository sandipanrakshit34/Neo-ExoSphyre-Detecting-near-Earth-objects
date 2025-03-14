# Neo-ExoSphyre-Detecting-near-Earth-objects
Neo ExoSphyre is an AI-driven project for detecting and tracking Near-Earth Objects (NEOs) like asteroids and comets. Using machine learning, it processes data to predict NEO trajectories and assess potential collision risks.

<center> <img src = "Assets/PIA00136~orig.jpg" width = 100%>

    ## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Project Index](#project-index)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [Project Roadmap](#project-roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

# overview

The **Near-Earth Object (NEO) Detection Simulation** project aims to optimize the observation strategy of NEOs by simulating their detection based on different telescope properties and observational parameters. With the growing catalog of NEOs (currently over 30,000), efficient detection and monitoring are crucial for planetary defense and space exploration. This project focuses on the use of Python to create a comprehensive tool that allows astronomers and space enthusiasts to explore the visibility and detection of NEOs based on various factors such as telescope settings, camera properties, and sky conditions.

By using a combination of data analysis, visualization, and simulation, this tool helps optimize survey strategies for NEO detection. The project covers the processing of NEO data, generating sky maps, simulating telescope observation settings, and computing detection probabilities. It provides valuable insights into how telescope configurations affect the discovery rate of NEOs and helps identify regions in the sky that are most promising for NEO surveys.

## Contributors:

<br/>
<div align="left">
    <table style="border-collapse: collapse; border: none;">
        <tr>
            <td align="center" style="border: none; text-align: center; padding: 10px;">
                <a href="https://github.com/sandipanrakshit34" target="_blank">
                    <img src="Assets/sandipan_rakshit.png" 
                         alt="sandipanrakshit34" 
                         width="140" height="140" 
                         style="border-radius: 50%;" />
                </a>
                <br>
                <strong><a href="https://github.com/sandipanrakshit34" style="text-decoration: none; color: #61dafb;">sandipanrakshit34</a></strong>
            </td>
            <td align="center" style="border: none; text-align: center; padding: 10px;">
                <a href="https://github.com/Niloy-Aiml34" target="_blank">
                    <img src="Assets/niloy_das.png" 
                         alt="Niloy-Aiml34" 
                         width="140" height="140"
                         style="border-radius: 50%;" />
                </a>
                <br>
                <strong><a href="https://github.com/Niloy-Aiml34" style="text-decoration: none; color: #61dafb;">Niloy-Aiml34</a></strong>
            </td>
            <td align="center" style="border: none; text-align: center; padding: 10px;">
                <a href="https://github.com/Mrigangana-Sarkar" target="_blank">
                    <img src="Assets/mriganga_sarkar.png" 
                         alt="Mrigangana-Sarkar" 
                         width="140" height="140"
                         style="border-radius: 50%;" />
                </a>
                <br>
                <strong><a href="https://github.com/Mrigangana-Sarkar" style="text-decoration: none; color: #61dafb;">Mrigangana-Sarkar</a></strong>
            </td>
        </tr>
    </table>
</div>


## Features
- **Interactive Sky Maps**: Visualize NEOs dynamically using `ipywidgets` and `matplotlib`, filtering by properties like apparent magnitude, class, and angular distance to the Sun.
- **NEO Population Modeling**: Simulate and analyze NEO distribution using population models, considering dynamical and physical properties.
- **Detection Simulation**: Simulate NEO visibility and detection rates based on telescope parameters such as exposure time, pixel size, and limiting magnitude.
- **Data Processing and Database**: Efficiently parse, store, and query NEO data in an SQLite database for streamlined analysis.
- **Detection Probability Maps**: Use Kernel Density Estimators (KDEs) from `scikit-learn` to generate detection probability maps, identifying regions of interest for NEO surveys.
- **Bias Analysis and Optimization**: Investigate detection biases and optimize future NEO survey strategies.

## Project Structure
The project is structured into several key components:
- **Data Collection**: Download and parse NEO data from the ESA NEODyS website.
- **Database Creation**: Store NEO data in an SQLite database for efficient querying.
- **NEO Classification**: Classify NEOs into categories (Amors, Apollos, Atens, Atiras) based on astro-dynamical properties.
- **Apparent Magnitude Calculation**: Compute NEO brightness using the H-G function.
- **Sky Map Visualization**: Create interactive sky maps for real-time exploration of NEO data.
- **Detection Simulation**: Simulate NEO detection based on telescope configurations.
- **Detection Probability Maps**: Generate KDE-based maps to identify high-density NEO regions.
- **Bias Analysis**: Analyze detection biases and optimize observation strategies

## Technologies Used

- **Python**: The core programming language used for all data processing, simulation, and visualization tasks.
- **SQLite**: A lightweight database to store and manage NEO data, including orbital elements and physical parameters.
- **Seaborn**: Used for statistical visualization, allowing for deep analysis of NEO properties like size distribution and orbital elements.
- **Matplotlib**: For generating static, animated, and interactive visualizations such as histograms, scatter plots, and sky maps.
- **Ipywidgets**: Enables interactive filtering and visualization within Jupyter Notebooks for real-time exploration of NEO data.
- **Scikit-learn**: Implements **Kernel Density Estimators (KDEs)** to compute NEO detection probability functions on sky maps, helping identify regions of interest.

## How It Works

1. **Data Collection and Database Creation**: 
   The project begins by downloading the latest NEO data from the **ESA NEODyS website**. This data includes orbital elements and physical parameters for NEOs, which are then parsed and stored in an **SQLite** database for efficient querying and analysis.    

2. **NEO Classification**: 
   The NEOs are classified into four major categories—**Amors**, **Apollos**, **Atens**, and **Atiras**—based on their astro-dynamical properties. This classification helps in better understanding the observational biases associated with different NEO types.

3. **Apparent Magnitude Calculation**: 
   Using the **H-G function**, the apparent magnitude of NEOs is computed to estimate their brightness as seen from Earth. This calculation is essential for determining which NEOs are observable based on the limiting magnitude of telescopes.

4. **Sky Map Visualization**: 
   The project provides an interactive **sky map** where users can filter NEOs based on various criteria such as apparent magnitude, angular distance to the Sun, and NEO class. This allows users to explore which regions of the sky are most promising for observation.

5. **Detection Simulation**: 
   The heart of the project is the simulation of NEO detection, considering different telescope properties like exposure time and pixel size. A **for-loop** is used to simulate the movement and appearance of NEOs over time, and detection rates are calculated based on the telescope’s configuration.

6. **Detection Probability Maps**: 
   Using **Kernel Density Estimators (KDEs)**, the project generates detection probability maps that display the density of NEOs in the sky. These maps help identify areas of the sky with higher concentrations of NEOs, optimizing observation strategies.

7. **Bias Analysis and Optimization**: 
   The project also investigates potential biases in the detection process, including those based on NEO population models and observational settings. By analyzing how telescope properties influence detection rates, the project helps improve future NEO survey strategies.

## Installation

To run the project, you'll need to have Python 3.x installed along with the required libraries. You can install all dependencies using the following command:

```bash
pip install -r requirements.txt

