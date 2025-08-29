# Static Image Processing Using Pynq z1
This Image Processing Project leverages the Xilinx PYNQ-Z1 board to perform real-time image processing and visualization. Utilizing Python and OpenCV, the project applies multiple image filters to a source image and outputs the results via an HDMI-connected monitor. This documentation outlines the setup, usage, code structure, and potential enhancements for the project.
## Requirements:
Hardware: PYNQ-Z1 board, HDMI monitor, HDMI cable, 12V power supply.
Software: PYNQ image installed on a microSD card, Jupyter notebook environment.
Libraries: Python with PIL, NumPy, Matplotlib, and OpenCV installed.
Bitstream: Compatible `base.bit` file for the PYNQ-Z1 overlay.
## Setup Guide:
1.	Insert the microSD card with the PYNQ image into the PYNQ-Z1 board.
2.	Connect the HDMI cable from the PYNQ-Z1 to the monitor and power on the board.
3.	Access the Jupyter notebook server via the PYNQ-Z1’s IP address in a web browser.
4.	Upload the source image `SourceImage.jpg` to `/home/xilinx/jupyter_notebooks/Image_Processing/`.
5.	Ensure the `base.bit` file is available in the working directory.
## Working:
### Cell 01:
The PYNQ-Z1 Image Processing Project code operates by loading a 640x480 image, converting it from RGB to BGR for OpenCV compatibility, and displaying it in the Jupyter notebook. 
###CELL 02:
Initializes the PYNQ-Z1 overlay and configures the HDMI output at 640x480 with 24-bit depth.
### CELL 03:
Applies filters—Grayscale, Threshold, Edge Detection, Blur, and Sharpening—using OpenCV, converts single-channel images to 3-channel BGR, and displays them in subplots.
![WhatsApp Image 2025-08-29 at 13 26 53_47782dc8](https://github.com/user-attachments/assets/2348dd44-e3c6-4992-bcc9-02537ef3d9b8)
### CELL 04:
Runs an interactive loop, prompting the user to select a filter (1-5) or exit (6), then writes the chosen 3-channel BGR image to the HDMI monitor, ensuring shape and dtype compatibility with a 1-second delay for updates.
![WhatsApp Image 2025-08-29 at 13 30 06_8eaa2bec](https://github.com/user-attachments/assets/1a7052a0-598e-4bc6-9e4a-53054b79c8e6)
## Results:
The greyscale Image of the original image is then displayed on the Monitor connected via HDMI to the PYNQ board.
![WhatsApp Image 2025-08-29 at 13 29 22_1a07d3b9](https://github.com/user-attachments/assets/b81311a4-d9b4-4e57-8747-1ff857ccb389)


