# PopupBench: Benchmarking Context-Aware Popup Handling in Vision-Language GUI Agents

**Anonymous Repository for ACL Submission**

This repository provides the official dataset for the paper *"PopupBench: Benchmarking Context-Aware Popup Handling in Vision-Language GUI Agents"*. 

Currently, this repository is dedicated **solely to sharing the dataset** for the double-blind review process. Evaluation scripts and Pop-LM training codes will be fully released upon acceptance.

## 📥 Dataset Download
The full dataset is approximately **2GB** in size and is hosted securely via an anonymous cloud storage link to comply with double-blind review policies.

* **Download Link:** [Click here to download the PopupBench Dataset](https://drive.google.com/file/d/1JI_jyDzflX1NrlYmJPieuA-KZ8DZOq_U/view?usp=sharing)

> **Note for Reviewers:** Please download the `.zip` file and extract it to your local environment.

## 📊 Dataset Overview
PopupBench is the first benchmark designed to evaluate how Vision-Language Models (VLMs) and GUI agents handle unexpected, context-dependent popups. 

The dataset consists of **9,862 test cases** in total, spanning across three environments:
* **Ubuntu (Synthetic):** Cases with varying popup interventions in a Linux desktop environment.
* **Windows (Synthetic):** Cases representing professional, cross-application workflows on Windows OS.
* **Real-Web:** In-the-wild cases collected from actual websites (e.g., cookie banners, login prompts).

### Task Definition
Each case requires the agent to determine the relevance of a popup to the current task:
1. **Related Popups:** The agent must interact with the popup to proceed with the task.
2. **Unrelated Popups:** The agent must dismiss the popup (e.g., clicking an 'X' or 'Cancel' button) before proceeding.

## 📁 Directory Structure
Upon extracting the downloaded zip file, the dataset is organized as follows:

```text
PopupBench_Dataset/
├── ubuntu_handmade_fullscreen/
│   ├── images/                                      # Synthetic cases with varying popup interventions on Ubuntu
│   └── dataset_synth_cases_merged_realistic.json    # Annotations and GT coordinates for Ubuntu
├── window_handmade_fullscreen/
│   ├── images/                                      # Professional cross-application workflow cases on Windows
│   └── dataset_synth_cases_merged_realistic.json    # Annotations and GT coordinates for Windows
└── web_real_fullscreen/
    ├── images/                                      # In-the-wild cases collected from actual websites
    └── dataset_synth_cases_merged_realistic.json    # Annotations and GT coordinates for Real-Web
