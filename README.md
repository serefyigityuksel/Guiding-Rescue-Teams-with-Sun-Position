# Guiding-Rescue-Teams-with-Sun-Position

This project aims to calculate the solar position (azimuth and altitude angles) using plant and shadow lengths from an image. By determining the solar position, the project can help guide search and rescue teams to locate objects or people based on the shadow cast.

![Ekran görüntüsü 2024-09-01 134027](https://github.com/user-attachments/assets/8993a988-6bda-4917-a197-a168937b6b83)


## Overview

The code performs the following tasks:
1. **Image Loading and Manual Selection:** Loads an image and allows the user to manually select points to determine plant and shadow lengths.
2. **Distance Calculation:** Calculates the real-world lengths of the plant and its shadow based on pixel measurements and a predefined scale factor.
3. **Solar Position Calculation:** Calculates the solar position using the azimuth and altitude angles, then determines the observer's location (latitude and longitude) based on the solar position.
4. **Observer Location Calculation:** Uses the Python ephem library to calculate the observer's location by taking into account the sun's right ascension and declination.

## Requirements
To run this code, you need to have the following Python libraries installed:
- OpenCV (cv2)
- NumPy
- Math
- datetime
- PyEphem (ephem)

## How to Use

1. **Prepare Your Image:** Ensure that your image is in the same directory as your script or provide the correct path to the image file. The image should clearly show a plant and its shadow.
2. **Run the Script:** Execute the script in your Python environment.
3. **Manual Selection:**
The script will display the image. Click four points on the image in the following order:
- Start of the plant
- End of the plant
- Start of the shadow
- End of the shadow
4. **View Results:** The script will calculate and display the following:
  - Plant and shadow lengths in pixels and meters.
  - Solar declination angle and solar hour angle.
  - Observer's latitude and longitude based on the calculated solar position.

## Future Improvements

- **Automated Detection:** Implement automatic detection of plant and shadow in the image using image processing techniques or machine learning.
- **Error Handling:** Add error handling for cases where fewer than four points are selected.
- **User Interface:** Develop a graphical user interface (GUI) for easier interaction.

## Issues and Suggetions

Although the focal length is known in the metadata of the image during manual point selection, in the example the final result is not accurate due to camera position and the distance between the objects are not known precisely. More precise calculations are needed to improve this study with the geodetic astronomy method and to reach more accurate results.
