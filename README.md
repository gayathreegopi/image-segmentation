# Image Segmentation Using Linear Programming and Max Flow Min Cut Theorem

This repository contains a novel tool for grayscale image segmentation that leverages linear programming, specifically the max flow/min cut theorem, to process images and separate foreground from background. The tool is designed to handle diverse image complexities efficiently, making it a robust solution for various segmentation tasks.

## Project Overview

The project applies the max flow/min cut theorem to represent each image as a flow network where pixels are treated as nodes, and edges represent the similarity between neighboring pixels. Using linear programming, the tool identifies optimal cuts that minimize the "water flow" between regions, segmenting images into foreground and background.

## Contributions

- **Image Processing**:
  - Handles both `.jpg` and `.csv` file formats.
  - Normalizes pixel intensities for stable model performance.
- **Flow Network Construction**:
  - Creates a sparse matrix to model pixel-based flow networks with source and sink nodes.
  - Uses depth-first search to identify accessible nodes.
- **Optimization**:
  - Utilizes Gurobi to solve the max flow problem and identify the minimum cut for segmentation.
- **Visualization**:
  - Reconstructs segmented images with clear foreground and background regions.

## Important Findings

1. **Precision in Segmentation**:
   - The tool delivers accurate cuts, outperforming conventional methods like Photoshop's Magic Wand tool.
2. **Scalability**:
   - Optimized with sparse matrices and linear programming, the model efficiently processes diverse image sizes.
3. **Automated Efficiency**:
   - The automated approach simplifies segmentation tasks for users without advanced image editing skills.

## Technologies Used

- **Programming Languages**: Python
- **Libraries and Tools**: NumPy, Gurobi, Matplotlib
- **Algorithms**: Max Flow/Min Cut Theorem

## How to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/image-segmentation-lp.git
   ```
2. **Install Dependencies**:
```bash
pip install -r requirements.txt
```
3.  **Run the Jupyter Notebook**:
Open Project 1.ipynb in Jupyter Notebook or JupyterLab.
Follow the provided instructions to load your image and execute the segmentation process.
4. **Output**:
Visualize the segmented image with clear foreground-background separation.

## Future Enhancements
* Scalability: Explore GPU-based acceleration to process high-resolution images faster.
* Generalization: Extend support for colored images and videos.
* Testing: Perform additional testing on complex images to improve segmentation accuracy in edge cases.

## Contact
For questions or further information, please contact:
* LinkedIn: [linkedin.com/in/gayathreegopi](https://linkedin.com/in/gayathreegopi)
