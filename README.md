# Repository introduction 
This repository is used to show the code and simulation results for the paper "Feature-Driven Multi-Agent Reinforcement Learning for UAV Trajectory Planning and Power Allocation in Dynamic Environments". We will update the whole experiment code after acceptance. Now, we just put the simulation results for algorithms PCNFD-MARL and GNNFD-MARL.

# Code-Structure
After the paper is accepted, we will update the code as the following structure:
```bash
FM-EAC/
├── Tokyo-map-Task/                                       # Urban scenario modeling and communication simulation
│   ├── city_map/                                # Original map dataset
│   ├── trace/                                   # Pedestrian movement trajectory dataset
environment
│   ├── physical_model.py                        # UAV kinematic and battery consumption  maps
│   ├── plot_building.py                         # 2D building distribution visualization
│   ├── plot_terrain.py                          # 3D rendering of terrain including buildings and elevation
│   ├── plot_traffic.py                          # Visualization of pedestrian traffic flow
 data
│   ├── EAC-PAN/                                 # PAN-based reinforcement learning for urban UAV deployment
│   │   ├── outputs/
│   │   │   ├── photos/                          # Output of various visualizations
│   │   │   ├── path/                            # UAV trajectory images
│   │   │   ├── reward/                          # Reward curve plots during training
│   │   │   └── results/                         # Numerical results: inference time and reward
│   │   ├── model/                               # Trained neural network weights and checkpoints
│   │   ├── feature_extraction.py                # Feature extraction and PAN model training
│   │   ├── pointarray_feature_extractor.pth     # Saved feature extraction model weights
│   │   ├── env.py                               # UAV environment simulation for reinforcement learning
│   │   ├── urban_eac_pan_model.py               # PAN + RL network architecture
│   │   ├── train.py                             # Main training pipeline
│   │   └── test.py                              # Model evaluation and testing
│   └── EAC-GNN/                                 # GNN-based reinforcement learning for urban UAVs
│       ├── outputs/
│       │   ├── photos/                          # Visualization outputs
│       │   ├── path/                            # UAV path plots
│       │   ├── reward/                          # Reward plots
│       │   └── results/                         # Inference and performance results
│       ├── model/                               # GNN model weights
│       ├── env.py                               # UAV flight environment for GNN-based learning
│       ├── urban_eac_gnn_model.py               # GNN + RL model architecture
│       ├── train.py                             # Training pipeline
│       └── test.py                              # Testing and evaluation
```

# Simulation Results
PSD traces figures are put in /Visualization Results/PSD_trace. 
This means the PSD traces were generated from SUMOTRACE. 
We processed this data, and for your convenience, we transformed the SUMO XML table into figures. 
For different city area location scenarios, we set some different PMP traces. 
The name x_y.png represents the visualization of scenario x and PMP trace y. 
As detailed, we chose 3 areas and 30 traces.

The example of PSD traces can be represented as:

<img width="1529" height="1228" alt="example_1" src="https://github.com/user-attachments/assets/03b60d3e-e259-4cb1-bf83-aa9b8212883e" />

About the UAV trajectories, we divide the visualization results into two categories. The trajectory figures for both GNNFD-MARL and PCNFD-MARL are provided as interactive “.png” files. This interactive format makes it convenient to observe the UAV flight trajectories and their maneuvering behavior among surrounding buildings. In addition, for each scenario, we also provide a static 2D top-down view in “.png” format. The 3D interactive view preserves altitude information and clearly illustrates how UAVs navigate above and around obstacles, while the 2D top-down view offers a concise, paper-friendly representation of planar paths that is suitable for quick comparison across scenarios or direct embedding into documents.
The visualization results are organized by algorithm and visualization mode as follows:
GNNFD-MARL results

3D: /visualization/3d/GNNFD

2D: /visualization/2d/GNNFD

PCNFD-MARL results

3D: /visualization/3d/PCNFD

2D: /visualization/2d/PCNFD

For each scenario, we assign different start points and destinations to four UAVs to perform the tasks. The scenarios correspond to the PSD trace filenames. Specifically, a file named map_i_trace_j.png represents the visualization result of scenario i with PSD trace j.
The example of GNNFD-MARL trajector can be represented as:

<img width="3229" height="2778" alt="gnn-2" src="https://github.com/user-attachments/assets/72fff33f-3d34-49a1-9cc3-98c344ecff8d" />


The example of PCNFD-MARL trajector can be represented as:

<img width="3158" height="2778" alt="pcn-2" src="https://github.com/user-attachments/assets/ff1ce113-6ee0-485c-87ce-3680cf2ab696" />


# Updates
``` Jun, 12, 2026: ``` Paper Re-submission.


