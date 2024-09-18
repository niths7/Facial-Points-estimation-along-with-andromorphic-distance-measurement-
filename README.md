# Facial-Points-estimation-along-with-andromorphic-distance-measurement

This project detects facial landmarks and calculates anthropological distances (like eye width, mouth width, philtrum length, etc.) using a reference scale of 30 cm. It utilizes OpenCV and Dlib to identify key facial features and estimate measurements in real-world dimensions (centimeters).

## Table of Contents

- [About](#about)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## About

This tool uses facial landmarks detected from an image and a manually selected reference scale to calculate various anthropological distances such as:

- Eye width
- Mouth width
- Philtrum length
- Upper face breadth
- Middle face length

It allows users to manually select a reference scale in an image (assumed to be 30 cm) to calibrate the measurements, converting pixel distances into real-world centimeters.

## Features

- Detects facial landmarks using Dlib's 68-point facial landmark predictor.
- Calculates anthropological distances such as eye width, mouth width, and philtrum length.
- Allows users to define a reference scale manually (in the image) for pixel-to-centimeter conversion.
- Draws the selected reference scale and landmark points on the image.
- Displays the calculated distances on the image.

## Requirements

- Python 3.x
- OpenCV (`cv2`)
- Dlib (`dlib`)
- NumPy (`numpy`)
- Matplotlib (`matplotlib`)

Make sure you have the pre-trained model file `shape_predictor_68_face_landmarks.dat`, which can be downloaded from [Dlib's website](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2).

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository
   ```

2. Install the required dependencies:

   ```bash
   pip install opencv-python dlib numpy matplotlib
   ```

3. Download the `shape_predictor_68_face_landmarks.dat` file from [here](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2), extract it, and place it in the project directory.

## Usage

1. Prepare your image and note the location of the reference scale (assumed to be 30 cm).
2. Run the script with your image file path:

   ```python
   python anthropological_distance.py
   ```

3. When the image appears:
    - Click to select two points on the image that define the reference scale (30 cm in real life).
    - The program will calculate the conversion factor based on this scale and detect facial landmarks to compute anthropological distances.
    - The distances will be drawn and printed on the image.

### Example Code Snippet

```python
image_path =  r"C:\Users\WELCOME\Downloads\kutty_paiyan.jpg"  # Replace with the path to your image
image = cv2.imread(image_path)
fig, ax = plt.subplots()
ax.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
ax.set_title('Select two points for reference scale (30 cm)')
selected_points = []
```

4. You will see printed output and visual annotations for:
    - Eye width
    - Mouth width
    - Philtrum length
    - Upper face breadth
    - Middle face length

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new feature branch (`git checkout -b feature/new-feature`).
3. Make your changes and commit (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

You can customize the project name, GitHub links, or additional details as needed.
