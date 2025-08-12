[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1dnebKVUScEyaFvcR5jWCJljafG7025nf?usp=sharing#scrollTo=WWRf3p-PUYln)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1EiK9IjsQqDq9hbtwngzoO7z62bH1qr1a#scrollTo=RR_pAuVrR2po)

Project Overview
Title: Modeling Human Visuomotor Coordination in Dual-Tasking using Deep Inverse Reinforcement Learning

Objective:
This project simulates and analyzes human full-body movements during dual-tasking—combining motor tasks (like walking) with cognitive tasks (such as task accuracy). First, synthetic data is generated and used to train Deep Inverse Reinforcement Learning (DIRL) models to learn reward functions. Later, real-world Vicon motion capture data is used to validate and refine these models. The ultimate goal is to model and predict human visuomotor coordination in complex, real-life dual-tasking environments.

Data Sources:

1. Synthetic Full-Body Dataset
A synthetic dataset was generated to simulate full-body joint angles and gait/cognitive metrics over time. This dataset includes:
arXiv

Lower Body Joints: Pelvis, hip, knee, tibia, ankle, foot, and toe angles.
Upper Body Joints: Head, spine, shoulder, arm, elbow, wrist, and hand angles.
Gait Metrics: Step length, step time, stride variability, ground reaction force.
Cognitive Metrics: Reaction time and task accuracy.

These features were simulated for multiple subjects over a specified duration and sampling rate.

Access the synthetic data generation notebook here:

2. Vicon-Based Dataset
The Vicon dataset provides real-world motion capture data, including:

Joint Angles: Detailed angles for various body joints during movement.
Gait Metrics: Stride length, cadence, and other spatiotemporal parameters.
Cognitive Metrics: Performance data during dual-task scenarios.

This dataset is used to validate and refine the models trained on synthetic data.

Data Preprocessing
Both datasets undergo preprocessing steps:
Normalization: Standard scaling of joint angles and metrics.
Feature Selection: Identification of relevant features for modeling.
Data Splitting: Division into training and testing sets.

Deep Inverse Reinforcement Learning (DIRL)

DIRL is employed to learn reward functions from the observed human behavior:
Reward Network Architecture: A neural network is designed to predict rewards based on input features.
Training: The network is trained using margin ranking loss to model the preference of higher task accuracy.
Evaluation: Performance is assessed by comparing predicted rewards with actual task accuracy.

Results:

The models trained on synthetic data demonstrate the ability to predict human task performance based on joint angles and gait metrics. When applied to the Vicon dataset, these models show promising results in generalizing to real-world data.
