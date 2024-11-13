# 🖼️ Generate-Custom-QR-Codes-with-Python 
This project is a QR Code Generator built in Python. It's a simple tool that creates QR codes for URLs, text, or any other data you want to encode. Perfect for linking to files in Google Drive, sharing links, or creating custom QR codes!

## ✨ Features
* Generate QR codes from any URL or text data.
* Customize QR code color (foreground and background).
* Display the QR code directly in Google Colab or Jupyter Notebook.
* Save the QR code as a PNG image for easy sharing.
  
## 📦 Requirements
To run this project, you need:
* Python 3.x
* Libraries: qrcode and Pillow (for image handling)

🚀 Installation
1. Clone this repository
``` bash
git clone https://github.com/lokeshvloki/qr-code-generator.git
```
``` bash
pip install qrcode[pil]
```
## 🔧 Usage
1. Open the project in Google Colab or Jupyter Notebook.
2. Replace the data variable with the URL or text you want to encode (for example, a Google Drive link).
3. Run the code, and your QR code will be generated instantly!
   
## 🔍 Example Code
Here’s an example of generating a QR code with a custom color scheme in Google Colab:
``` python
# Import necessary libraries
import qrcode
from PIL import Image
import matplotlib.pyplot as plt

# Replace 'data' with your Google Drive link or other data
data = "https://drive.google.com/your-file-link"

# Create a QR code instance
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_L,
    box_size=10,
    border=4,
)

# Add data to the QR code
data = "https://drive.google.com/file/d/1-4HNRmxW8it/view?usp=drivesdk"
qr.add_data(data)
qr.make(fit=True)


# Create an image of the QR Code with Specified colors
img = qr.make_image(fill_color="black", back_color="white")

# Display the image in Google Colab
plt.imshow(img, cmap='gray')
plt.axis('off')  # Hide axes
plt.show()
```
## 💾 Saving the QR Code
To save the QR code as a PNG image, use this command:
``` python
img.save("qr_code.png")
```
## 🧪 How It Works
1. Data Encoding: The add_data function encodes the data (URL, text, etc.) into the QR code.
2. Customization: Customize colors with fill_color and back_color.
3. Display: Use the display(Image(...)) function to show the image directly in Colab or Jupyter.

## 🤝 Contributing
Contributions are welcome! Feel free to fork the repo, make your changes, and submit a pull request. Together, we can make this tool even better! 


## 📬 Contact
For questions or suggestions, reach out to Lokesh V at lokeshv2403@gmail.com
