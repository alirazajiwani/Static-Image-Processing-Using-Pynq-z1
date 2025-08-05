# Static Image Processing Using Pynq z1
The Pynq-Z1 Image Processing Project leverages the Xilinx PYNQ-Z1 board to perform real-time image processing and visualization. Utilizing Python and OpenCV, the project applies multiple image filters to a source image and outputs the results via an HDMI-connected monitor. This documentation outlines the setup, usage, code structure, and potential enhancements for the project.
## Requirements:
Hardware: PYNQ-Z1 board, HDMI monitor, HDMI cable, 12V power supply.
Software: PYNQ image  installed on a microSD card, Jupyter notebook environment.
Libraries: Python with PIL, NumPy, Matplotlib, and OpenCV installed.
Bitstream: Compatible `base.bit` file for the PYNQ-Z1 overlay.
## Setup Guide:
1.	Insert the microSD card with the PYNQ image into the PYNQ-Z1 board.
2.	Connect the HDMI cable from the PYNQ-Z1 to the monitor and power on the board.
3.	Access the Jupyter notebook server via the PYNQ-Z1’s IP address in a web browser.
4.	Upload the source image `SourceImage.jpg` to `/home/xilinx/jupyter_notebooks/Image_Processing/`.
5.	Ensure the `base.bit` file is available in the working directory.
## Working:
The PYNQ-Z1 Image Processing Project code operates by loading a 640x480 image in CELL 01, converting it from RGB to BGR for OpenCV compatibility, and displaying it in the Jupyter notebook. CELL 02 initializes the PYNQ-Z1 overlay and configures the HDMI output at 640x480 with 24-bit depth. CELL 03 applies filters—Grayscale, Threshold, Edge Detection, Blur, and Sharpening—using OpenCV, converts single-channel images to 3-channel BGR, and displays them in subplots. CELL 04 runs an interactive loop, prompting the user to select a filter (1-5) or exit (6), then writes the chosen 3-channel BGR image to the HDMI monitor, ensuring shape and dtype compatibility with a 1-second delay for updates.
