# Toward A Data-driven Cyberinfrastructure Tool for Urban Micromobility-Friendly Path Planning: A Hartford Study

Official materials for the ACM SIGSPATIAL 2026 paper:

Toward A Data-driven Cyberinfrastructure Tool for Urban Micromobility-Friendly Path Planning: A Hartford Study

## Overview

Micromobility Infrastructure Planner for Low-Stress and Accessible Networks (M-PLAN) is an algorithm for growing low-stress bike networks for micromobility that analyzes OpenStreetMap (OSM) data to identify bike infrastructure, assign stress levels based on road attributes, and recommend targeted upgrades.

## Algorithm Overview

The tool follows a five-step process to generate an optimized network:

1.  **Data Acquisition & Preprocessing:** Downloads and cleans OSM data for a specified study area.
2.  **Traffic Stress Modeling:** Assigns a binary stress level (High/Low) to road segments based on custom logic and road attributes.
3.  **Network Expansion:** Uses a Minimum Spanning Tree (MST) algorithm to efficiently expand the network and connect fragmented segments, minimizing infrastructure costs.
4.  **Connectivity Evaluation:** Applies Dijkstra's algorithm to assess the overall low-stress connectivity to key destinations (Points of Interest).
5.  **Real-World Validation:** Automatically retrieves Google Maps Street View images for proposed upgrades to confirm feasibility.

## Getting Started

This project is set up to run directly in the **Google Colaboratory (Colab)** environment.

### Prerequisites

* A Google account (required to run Colab).
* A polygon shapefile of the desired study area. 
* A **Google Maps Street View Static API Key** is required for the final `Real-World Validation` step. Instructions for inserting this key are provided in the notebook.

## Abstract

The increasing demand for sustainable and affordable urban mobility and connectivity has underscored the need for cohesive, micromobility-friendly paths as well as micromobility networks, serving both cyclists and electric (e)-scooter riders. To this end, this paper aims to explore and investigate how to (1) evaluate the micromobility network connectivity as well as their friendliness and stress for riding micromobility vehicles; and (2) recommend connection of fragmented micromobility networks and their upgrades within a city. To this end, we present a Micromobility infrastructure Planner for Low-stress and Accessible Networks (M-PLAN), a geospatial cyberinfrastructure tool for planning support of micromobility-friendly, user-centered networks. M-PLAN analyzes OpenStreetMap (OSM) as well as Hartford’s Bicycle Master Plan data to identify existing micromobility infrastructures, determines micromobility stress levels based on geospatial attributes, and recommends targeted upgrades and network expansions. Our tool applies a Minimum Spanning Tree (MST) algorithm to expand networks, and integrates Dijkstra’s algorithm to evaluate low-stress connectivity to destinations. Our real-world case studies in the City of Hartford, Connecticut (CT) have demonstrated the M-PLAN’s effectiveness in identifying infrastructure gaps and recommending improvements for low-stress, connected micromobility networks. The M-PLAN cyberinfrastructure project will have broad impacts in serving the geospatial research communities and beyond.

## Acknowledgments
This project builds upon and was inspired by prior work, including:

- [BikeDNA](https://github.com/anerv/BikeDNA), licensed under AGPL-3.0  
- [bikenwgrowth](https://github.com/mszell/bikenwgrowth), licensed under AGPL-3.0   
- [PeopleForBikes City Ratings methodology](https://cityratings.peopleforbikes.org/about/methodology)  
