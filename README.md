# Generative_Art
Scripts for generative art
Please cite this repository if you use any of these scripts in your projects.

## 1. Adjacency_matrix_from_image.ipynb

*Works best with images with multiple objects. Plotting relationships between different object classifications based on Euclidian distances.*

<img width="1593" height="682" alt="image" src="https://github.com/user-attachments/assets/fe63550b-2855-41a9-976f-6fba1d82908e" />

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/irmakoz1/Generative_Art/blob/main/Adjacency_matrix_from_image.ipynb)



| Section                   | Summary                                                                                                                                                                                                                                                                                                            |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Algorithm**             | 1. Detect objects using YOLO (`yolov8n.pt`).<br>2. Extract bounding boxes, class labels, and IDs.<br>3. Compute pairwise Euclidean distances between object centers.<br>4. Normalize distance by image diagonal.<br>5. Create edge if distance < threshold (`d_norm < 0.3`).<br>6. Save adjacency info to CSV/TXT. |
| **Visualization**         | - Plot adjacency matrix using Matplotlib.<br>- Can display side-by-side with original image.<br>- Save plots with unique timestamped filenames.                                                                                                                                                                    |
| **Accuracy Improvements** | - Use higher-accuracy YOLO (`yolov8m.pt` / `yolov8l.pt`).<br>- Adjust `conf` and `IoU` thresholds.<br>- Draw bounding boxes for verification.<br>- Improve distance calculation (consider object size / perspective).<br>- Use dynamic edge thresholds.<br>- Apply class-based rules for meaningful edges.         |

