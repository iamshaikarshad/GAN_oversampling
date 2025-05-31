# GAN-Based Oversampling for Customer Retention Prediction

This project implements a Generative Adversarial Network (GAN) to address class imbalance in customer retention datasets.
By generating synthetic samples for the minority class, the model aims to improve the performance of classification algorithms in predicting customer retention.

## Overview

Class imbalance is a common issue in predictive modeling, where the number of instances in one class significantly outnumbers the other.
Traditional oversampling techniques like SMOTE or random oversampling may not capture the underlying data distribution effectively.
This project leverages GANs to generate realistic synthetic data for the minority class, thereby enhancing the classifier's ability to learn from balanced data.

## Project Structure

- **`retention_Oversampling_Gan.ipynb`**: Jupyter Notebook containing the implementation of the GAN model for oversampling.
- **`data/`**: Directory containing the dataset used for training and evaluation.
- **`models/`**: Directory to save trained models and generated synthetic data.
- **`README.md`**: Project documentation.

## Conceptual Diagram

Below is a conceptual diagram illustrating the GAN-based oversampling process:

```
[Minority Class Data] --> [Generator] --> [Synthetic Data]
                                     |
                                     v
[Real Data] --> [Discriminator] <--> [Synthetic Data]
                                     |
                                     v
                            [Improved Classifier]
```

In this setup:
- The **Generator** creates synthetic data resembling the minority class.
- The **Discriminator** evaluates the authenticity of the synthetic data against real data.
- The **Classifier** is trained on the augmented dataset, leading to improved performance.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/iamshaikarshad/GAN_oversampling.git
   cd GAN_oversampling
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Prepare the dataset:**
   - Place your dataset in the `data/` directory. Ensure it is in CSV format with appropriate preprocessing.

2. **Run the Jupyter Notebook:**
   ```bash
   jupyter notebook retention_Oversampling_Gan.ipynb
   ```

3. **Follow the steps in the notebook:**
   - Load and preprocess the data.
   - Train the GAN model to generate synthetic minority class samples.
   - Augment the original dataset with synthetic samples.
   - Train and evaluate the classifier on the balanced dataset.

## Results

The GAN-based oversampling approach demonstrated improved classification metrics compared to traditional oversampling methods.
By generating realistic synthetic data, the classifier achieved higher accuracy and better generalization on unseen data.

## References

- Chawla, N. V., et al. (2002). "SMOTE: Synthetic Minority Over-sampling Technique." Journal of Artificial Intelligence Research, 16, 321–357.
- Goodfellow, I., et al. (2014). "Generative Adversarial Nets." Advances in Neural Information Processing Systems, 27.
- FrancescoFanchin/GAN_Oversampling: Master's thesis - GitHub (https://github.com/FrancescoFanchin/GAN_Oversampling)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
