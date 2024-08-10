# API Reference

## `genqr.py`
This module provides the `genqr` function for generating QR codes with customizable features.

### **Imports**
- `qrcode` (qrcode): The library used for generating QR codes.
- `PIL.Image` (PIL): The Python Imaging Library for handling images.
- `io` (io): A module used for working with streams and memory buffers.

### **Functions**

#### `genqr(data=None, color="black", size=10, qr_border=5, qrversion=5)`
Generates a QR code with the specified parameters and returns it as a memory buffer.

- **Parameters:**
  - `data` (`str`, optional): The data to encode in the QR code. Default is `None`. Returns an error message if not provided.
  - `color` (`str`, optional): The color of the QR code. Default is `"black"`.
  - `size` (`int`, optional): The size of each box in the QR code, determining the resolution. Default is `10`.
  - `qr_border` (`int`, optional): The width of the border around the QR code in boxes. Default is `5`.
  - `qrversion` (`int`, optional): The version of the QR code, which controls the size and data capacity. Must be between `1` and `40`. Default is `5`.

- **Returns:**
  - `io.BytesIO`: A memory buffer containing the QR code image if successful.
  - `str`: An error message if an error occurs during the QR code generation process.

## `genqr.py`

This script uses the Streamlit framework to create a web interface for generating QR codes with custom data, color, version, border, and resolution.

### **Imports**
- `streamlit` (st): The Streamlit library for creating web apps.
- `genqr` (function): A custom function from `qr.py` to generate QR codes.
- `PIL.Image` (PIL.Image): The Python Imaging Library for handling images.

### **Streamlit App Components**

- **Title:**
  - `st.title()`: Displays the title of the web app. 
  - Content: `':violet[Gen]:rainbow[QR] 🌚'`.

- **Form:**
  - `st.form("custom-qr")`: Defines a form to collect user input for generating QR codes.
    - `st.text_input()`: Field for entering the data to encode in the QR code.
    - `st.color_picker()`: Color picker for selecting the QR code color.
    - `st.slider()`: Sliders for selecting QR version, border size, and resolution.

- **Submission:**
  - `st.form_submit_button("Submit")`: Button to submit the form.
  - Conditional logic to handle empty data input and errors during QR code generation.

- **QR Code Display:**
  - `st.image()`: Displays the generated QR code image.
  - `st.error()`: Displays error messages if any issues occur.
