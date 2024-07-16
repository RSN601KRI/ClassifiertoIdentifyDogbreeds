# Image Classifier: Dog Breed Identification

## Overview

This project aims to develop an image classification system to identify dog breeds using deep learning models. The classifier leverages pre-trained models from the PyTorch library, including ResNet18, AlexNet, and VGG16, to achieve accurate breed identification from images.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Models](#models)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Installation

### Prerequisites

- Python 3.10+
- pip (Python package installer)

### Dependencies

Install the required dependencies using the following command:

```bash
pip install -r requirements.txt
```

### Cloning the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/dog-breed-classifier.git
cd dog-breed-classifier
```

## Usage

### Running the Classifier

To run the image classifier, execute the following command:

```bash
python check_images.py --dir <directory_with_images> --arch <model_name> --dogfile <dogfile.txt>
```

- `--dir`: Directory containing images to classify.
- `--arch`: Model architecture to use (`resnet18`, `alexnet`, `vgg16`).
- `--dogfile`: Text file containing the list of dog breeds.

### Example

```bash
python check_images.py --dir pet_images --arch vgg16 --dogfile dognames.txt
```

### Understanding the Output

The classifier will output the classification results, including statistics such as the number of correctly classified dog images, breed matches, and overall accuracy.

## Project Structure

```
dog-breed-classifier/
│
├── check_images.py                # Main script to run the classifier
├── calculates_results_stats.py    # Script to calculate statistics from results
├── get_input_args.py              # Script to parse command line arguments
├── classifier.py                  # Script to load and use the classifier model
├── requirements.txt               # List of required dependencies
├── README.md                      # Project documentation
├── pet_images/                    # Directory containing sample images
├── dognames.txt                   # File containing dog breed names
└── results/                       # Directory to store output results
```

## Models

This project uses the following pre-trained models from the PyTorch library:

- **ResNet18**: A residual neural network with 18 layers.
- **AlexNet**: A convolutional neural network known for its role in popularizing deep learning.
- **VGG16**: A deep convolutional neural network with 16 layers.

### Switching Models

You can switch between different models by specifying the `--arch` argument when running the classifier. For instance, to use ResNet18, set `--arch resnet18`.

## Results

The `calculates_results_stats.py` script computes various statistics from the classification results, such as:

- Number of images
- Number of dog images
- Number of non-dog images
- Number of matches between pet and classifier labels
- Number of correctly classified dogs and breeds
- Percentage accuracy for matches, dogs, breeds, and non-dogs

### Example Output

![output](https://github.com/user-attachments/assets/9050259c-0201-4184-80e8-095f18012951)

```plaintext
Number of Images: 40
Number of Dog Images: 30
Number of Non-Dog Images: 10
Number of Matches: 36
Correctly Classified Dogs: 28
Correctly Classified Breeds: 25
Percentage Match: 90.0%
Percentage Correct Dogs: 93.3%
Percentage Correct Breeds: 83.3%
Percentage Correct Non-Dogs: 80.0%
```

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request for any improvements, bug fixes, or new features.

### Steps to Contribute

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- The PyTorch community for providing the pre-trained models.
- The Udacity team for the initial project idea and structure.

#Keep learning!🚀✨
