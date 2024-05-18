
# AI-Driven Freezing of Gait (FOG) Detection in Parkinson's Disease

## Overview
This repository contains the final project for the course "Applied AI – Academic Perspectives: AI & Health" by Iñigo Aduna and Ahmad Beigrezaei from KU Leuven. The project aims to enhance the detection and management of Freezing of Gait (FOG) in Parkinson's disease using AI and machine learning techniques.

## Authors
- Iñigo Aduna, KU Leuven (Brugge)
  - Email: inigo.adunaalonso@student.kuleuven.be
- Ahmad Beigrezaei, KU Leuven (Brugge)
  - Email: ahmad.beigrezaei@student.kuleuven.be

## Project Structure
- `Inigo_Ahmad_AI_Health_Project_Final.pdf`: Final project report detailing the methodologies, experiments, and results.
- `Exercise_FOG.ipynb`: Jupyter Notebook with code implementations and visualizations for the project.

## Table of Contents
1. [Introduction](#introduction)
2. [Data Availability](#data-availability)
3. [Methodologies](#methodologies)
    - [First Approach](#first-approach)
    - [Second Approach](#second-approach)
    - [Third Approach](#third-approach)
4. [Results and Analysis](#results-and-analysis)
5. [Conclusion](#conclusion)
6. [Future Work](#future-work)
7. [Bibliography](#bibliography)

## Introduction
Freezing of Gait (FOG) is a common symptom of Parkinson's disease characterized by a brief, episodic absence or marked reduction of forward progression of the feet despite the intention to walk. It severely impacts the quality of life, leading to falls and a loss of independence.

### State of the Art in FOG Monitoring
Current FOG monitoring involves inertial measurement units (IMUs) placed on the patient’s body to record movement patterns during FOG episodes. However, these systems are complex, costly, and require professional setup and maintenance.

### The Role of AI in Optimizing FOG Management
AI can automate the analysis of sensor data, providing real-time predictions of FOG episodes and enabling personalized treatment adjustments.

## Data Availability
The dataset comprises data from seven patients, each equipped with six sensors located on the chest, lumbar region, left and right ankles, and left and right feet. The dataset includes 2,554 files, each representing a two-second window with 256 rows and 36 columns of sensor data.

## Methodologies
### First Approach
- **Train-Test 80/20 Split**: Data from three accelerometers at the lumbar level were used to train a CNN model. Despite reasonable accuracy (82%), the model showed significant class imbalance issues.
- **Leave-One-Subject-Out (LOSO) Cross Validation**: Applied to evaluate the model's performance on unseen patients, revealing subject-specific variability.
- **Class Weighting**: Improved the F1 score for FOG detection by assigning greater weights to the minority class.

### Second Approach
- **Correlation Analysis**: Identified redundant signals to optimize sensor selection. This approach increased average accuracy to 75% but highlighted the need for better handling of class imbalance.

### Third Approach
- **Frequency Domain Analysis**: Utilized Discrete Fourier Transform (DFT) to analyze relevant frequency ranges associated with Parkinson's symptoms. This method showed potential but required further refinement.

## Results and Analysis
- **First Approach**: Highlighted class imbalance issues; improvements seen with class weighting.
- **Second Approach**: Sensor optimization showed mixed results, with some improvements in accuracy but challenges with overfitting.
- **Third Approach**: Frequency-based analysis offered a novel perspective but yielded slightly lower performance than time-domain analysis.

## Conclusion
AI and machine learning techniques offer significant potential for improving FOG detection and management in Parkinson's disease. Addressing class imbalance and optimizing sensor selection are crucial steps for future work.

## Future Work
- **Synthetic Data Generation**: Techniques like SMOTE to balance the dataset.
- **Ensemble Learning**: Combining multiple models to enhance generalization.
- **Multi-Domain Feature Integration**: Leveraging both temporal and frequency features.
- **Adaptive Models**: Tailoring models to individual patient profiles for more accurate FOG detection.

## Bibliography
1. Nutt JG, Bloem BR, Giladi N, et al. Freezing of gait: moving forward on a mysterious clinical phenomenon. *Lancet Neurol.* 2011;10(8):734-44. doi: [10.1016/S1474-4422(11)70143-0](https://doi.org/10.1016/S1474-4422(11)70143-0).
2. Krizhevsky A, Sutskever I, Hinton GE. ImageNet Classification with Deep Convolutional Neural Networks. *University of Toronto*.
3. O'Day J, Lee M, Seagers K, et al. Assessing inertial measurement unit locations for freezing of gait detection and patient preference. *J Neuroeng Rehabil.* 2022;19(1):20. doi: [10.1186/s12984-022-00992-x](https://doi.org/10.1186/s12984-022-00992-x).

## How to Use
1. Clone the repository.
   ```bash
   git clone https://github.com/username/FOG-Detection.git
   ```
2. Navigate to the project directory.
   ```bash
   cd FOG-Detection
   ```
3. Open the Jupyter Notebook.
   ```bash
   jupyter notebook Exercise_FOG.ipynb
   ```

## License
This project is licensed under the MIT License. See the LICENSE file for details.
