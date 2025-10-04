# Repository introduction 
This repository is used to show the code and simulation results for the paper "Feature-Driven Multi-Agent Reinforcement Learning for UAV Trajectory Planning and Power Allocation in Dynamic Environments". We will update the whole experiment code after acceptance. Now, we just put the simulation results for algorithms PCNFD-MARL and GNNFD-MARL.

# Code-Structure
After the paper is accepted, we will update the code as the following structure:
```bash
FM-EAC/
├── Tokyo-map-Task/                                       # Urban scenario modeling and communication simulation
│   ├── city_map/                                # Original TIFF map dataset
│   ├── city_map_cropped/                        # Cropped map images used for simulation
│   ├── trace/                                   # Pedestrian movement trajectory dataset
│   ├── antenna.py                               # Beamforming and antenna simulation
│   ├── cap.py                                   # Generates QoS-SINR relationship figures
│   ├── channel.py                               # Wireless channel capacity calculation
│   ├── communication.py                         # UAV communication model with the environment
│   ├── physical_model.py                        # UAV kinematic and battery consumption modeling
│   ├── crop_fig.py                              # Automated TIFF cropping script
│   ├── store_dsm.py                             # Store DSM (Digital Surface Model) height maps
│   ├── plot_antenna.py                          # Visualization of antenna patterns
│   ├── plot_building.py                         # 2D building distribution visualization
│   ├── plot_terrain.py                          # 3D rendering of terrain including buildings and elevation
│   ├── plot_traffic.py                          # Visualization of pedestrian traffic flow
│   ├── signal_map.py                            # Generate SINR heatmaps based on simulation data
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


# Simulation Results
PMP traces figures are put in /Visualization Results/PMP_trace. 
This means the PMP traces were generated from SUMOTRACE. 
We processed this data, and as convenience to know the details, we transformed the SUMO XML table into figures. 
For different city area location scenarios, we set some different PMP traces. 
The name x_y.png represents the visualization of scenario x and PMP trace y. 
As detailed, we chose 3 areas and 30 traces.

About the UAV trajectories, we divided them into two parts.
GNNFD-MARL and PCNFD-MARL trajectory figures are saved as ".html" files, which can be rotated, dragged, and viewed with details.
This is for the convenience of seeing the detailed trajectory and traces among buildings.
GNNFD-MARL trajectory figures are saved at /Visualization Results/GNNFD-MARL Trajectory Results.
PCNFD-MARL trajectory figures are saved at /Visualization Results/PCNFD-MARL Trajectory Results.
We choose different start points and destinations for 4 UAVs to perform tasks.

# Contact with Us
If you have any questions, please do not hesitate to contact us at this email: usainzhou@g.ecc.u-tokyo.ac.jp.

The scenarios correspond to the PMP trace filename.
The name map_i_trace_j.html represents the visualization of scenario i and PMP trace j.
