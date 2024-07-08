# Network Traffic VPN Classifier

This project aims to classify network traffic as VPN or Non-VPN using a Random Forest classifier. The model is trained on a dataset with various features extracted from network traffic and saved for future use.

## Project Structure

- `nt_vpn_classifier.ipynb`: Jupyter notebook containing the code to train and evaluate the Random Forest model.
- `network_vpn_classifier.pkl`: Saved model file for the Random Forest classifier.
- `README.md`: Project documentation.

## Prerequisites

Before running the project, ensure you have the following installed:

- Python 3.x
- Jupyter Notebook
- Required Python packages

## Installation

1. **Clone the Repository**:
   ```
   git clone git@github.com:akaasula21/network-traffic-classification.git
   cd network-traffic-classification
   ```

2. Create a Virtual Environment (optional but recommended):

    ```
    python -m venv nt_classi_env
    source nt_classi_env/bin/activate  # On Windows, use `nt_classi_env\Scripts\activate`
    ```

3. Install Required Packages:

    ```
    pip install -r requirements.txt
    ```

## Usage:

### Training the Model

1. Open Jupyter Notebook:

    ```
    jupyter notebook
    ```

2. Run the Notebook:

    Open nt_vpn_classifier.ipynb in Jupyter Notebook.
    Execute the cells to load the dataset, preprocess the data, train the model, and evaluate its performance.

3. Save the Model:

    After training, the model is saved as network_vpn_classifier.pkl.

### Using the Saved Model

To use the saved model for predictions, follow these steps:

1. Load the Model:

    ```
    import joblib
    model = joblib.load('network_vpn_classifier.pkl')
    ```

2. Make Predictions:

    Prepare your input data to match the features used during training.
    Use the model to make predictions:
    ```
    predictions = model.predict(input_data)
    ```

## Project Details

### Features used:

- Duration
- Total FIAT
- Total BIAT
- Min FIAT
- Min BIAT
- Max FIAT
- Max BIAT
- Mean FIAT
- Mean BIAT
- Flow Packets Per Second
- Std FIAT
- Min Active
- Mean Active
- Max Active
- Std Active
- Min Idle
- Mean Idle
- Max Idle

### Model:

    Random Forest Classifier

### Evaluation Metrics:

    Accuracy, Precision, Recall, F1-Score

## Contributing
    Contributions are welcome! Please fork the repository and submit a pull request for any improvements or additions.

## License
    This project is licensed under the MIT License.

## Acknowledgements

    Thanks to the dataset providers for making this project possible.
    Special thanks to the Python and machine learning communities for their support and resources.








