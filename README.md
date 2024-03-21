# AGM Growth Initiatives: Delivery Network Optimization

## Introduction

Acme Gourmet Meals (AGM) is a thriving startup that emerged from the vision of Joy, a former sous chef with a passion for healthy, gourmet meals. Recognizing the market's demand for convenient yet nutritious food options, Joy established AGM to provide fresh, high-quality meals tailored to busy professionals' lifestyles.

Recognizing the company's need to embrace emerging technologies, the data science team, management is exploring the potential of NoSQL databases such as Neo4j, MongoDB, and Redis. Aligning with AGM's vision for future growth, your team aims to leverage these technologies to optimize operations, enhance customer experiences, and support innovative delivery methods, including public transportation integration and drone deliveries.

Additionally, management is exploring various growth levers to propel AGM's expansion:
- Adding more pickup locations to improve accessibility and convenience for customers.
- Utilizing public transportation, such as BART, to transport deliveries, mitigating traffic congestion and enhancing efficiency.
- Implementing delivery drones and robots for localized deliveries, offering swift and convenient service within a limited range.
- Exploring hybrid combinations, such as pickup locations at BART stations, to capitalize on foot traffic and streamline delivery logistics.

## Goals
- Assess mode of transport AGM should use for its delivery services
- Employ data science methods, including graph-based algorithms to optimize AGM's network of pickup locations
- Assess the role of key NoSQL databases (Neo4j, MongoDB, and Redis) for implementing AGM's growth strategy

## Dataset

The project utilizes a dataset encompassing census data and geographical data points related to the BART transport network. This includes information on BART stations, lines between stations, and travel times between stations.

## Methodology

1. **Graph Creation and Data Preprocessing**: Initiating our analysis with the construction of a graph model to represent AGM's delivery network, including stations, routes, and connections. This phase involves cleaning and consolidating data of the BART network into a structured format that facilitates complex network analysis.
2. **Target Area Identification**: Pinpointing zip codes within the Bay Area with the highest potential for growth, based on current customer distribution and demographic insights.
3. **Geographical Analysis**: Leveraging spatial data to understand our operational environment and identify strategic areas for expansion.
4. **Network Optimization**: Extracting graph-based and demographic features and applying a sequential selection algorithm for our pickup locations, ensuring maximum efficiency and coverage.
5. **Impact Assessment**: Evaluating the potential impact of proposed changes on customer reach and service quality.

## Results

The analysis indicates promising avenues for network optimization, including potential locations for new pickup points for improved efficiency. By strategically placing 9 additional pickup locations based on our analysis, we can potentially extend AGM's service coverage to encompass 53.7% of the Bay Area's population within a 5-mile radius, up from 8.3% in its current situation. This expansion represents a substantial increase in AGM's market penetration and accessibility, positioning AGM to better meet the demands of its target customer base.

## Usage

Note that this project requires access to Neo4j and an external postgres database connected to python using psycopg2.

Libraries used are listed in the `requirements.txt` file.

## Contributors

- [Gary Kong]
- [Luis Garcia Lizaran]

## Project Organization

Below is the structure of our project repository:

    ├── LICENSE                                                         <- The license file for this project.
    ├── README.md                                                       <- The top-level README for developers using this project.
    ├── data
    │   ├── external                                                    <- External data files, including GeoJSON data and the BART map.
    │   │   ├── bart_map.png                                            <- Map of BART stations.
    │   │   └── geojson_data                                            <- GeoJSON files for various geographical regions.
    │   └── raw                                                         <- The original, immutable data dump.
    │       ├── census_data.csv                                         <- Census data for demographic analysis.
    │       ├── lines.csv                                               <- Data on BART lines for network analysis.
    │       ├── stations.csv                                            <- Information on BART stations.
    │       └── travel_times.csv                                        <- Travel times between stations.
    │
    ├── notebooks                                                      <- Jupyter notebooks for exploration and analysis.
    │   ├── 1.0-graph-creation.ipynb                                    <- Notebook for creating the graph-based model of the delivery network.
    │   └── 2.0-analysis.ipynb                                          <- Notebook for the analysis and optimization of the delivery network.
    │
    ├── reports                                                        <- Generated analysis reports and presentations.
    │   ├── AGM-DeliveryNetworkOptimization_Presentation_vF.pdf        <- Final presentation in PDF format.
    │   └── AGM-DeliveryNetworkOptimization_Presentation_vF.pptx       <- Final presentation in PowerPoint format.
    │
    └── requirements.txt                                                <- The requirements file for reproducing the analysis environment.
