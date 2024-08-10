# Getting Started with GenQR 
### A Streamlit App for Generating Colorful QR Codes. </br>
![Demo](demo.gif)
This script is a Streamlit-based web application that enables users to create QR codes with customizable features such as data, color, version, border, and resolution. The generated QR code is displayed as an image on the web page.

## Usage

To run this app, ensure you have the Streamlit framework installed along with the required libraries (`qr.py` module and PIL).

## 1. Title
The app title is displayed as **GenQR 🌚** with custom styling for an aesthetically pleasing interface.

## 2. Form
- **Data**: Input the data you want to encode into the QR code.
- **Color**: Choose a color for your QR code using a color picker.
- **Version**: Select the QR code version (ranges from 1 to 25).
- **Border**: Adjust the border width of the QR code.
- **Size**: Define the resolution of the QR code by selecting the size.

## 3. Submit
After configuring the QR code settings, click the **Submit** button to generate the QR code.

## 4. Error Handling
If no data is provided or an error occurs during QR code generation, an appropriate error message is displayed.