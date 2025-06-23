# edunet-virtual-internship - Secure Medical Image Steganography

This project embeds encrypted patient information inside medical images using Least Significant Bit (LSB) steganography and AES encryption with MAC authentication. It provides a secure way for healthcare systems to protect sensitive data while maintaining the visual integrity of medical scans.

## Features

- AES-256 Encryption with CBC mode
- HMAC-SHA256 for message integrity
- Patient data is hidden inside images using LSB
- Image quality is preserved (SSIM ~1.0)
- Changes are visually imperceptible but detectable with difference maps

## How It Works

1. Patient data is encrypted using AES (CBC) and protected using HMAC.
2. The encrypted message is converted to binary.
3. Binary bits are embedded into the image’s LSB (blue channel).
4. The system can later extract, verify, and decrypt the message securely.

## Requirements

- Python 3.8+
- OpenCV
- PyCryptodome
- NumPy
- scikit-image
- Matplotlib

Install all dependencies.

## Example Use Case

> A doctor embeds a patient’s ID and diagnosis inside a CT image securely before sending it to a specialist. The specialist can extract and decrypt the data using the shared password, ensuring both confidentiality and data integrity.

## License

This project is for academic and educational use only. Please consult with your institution before using it in real medical workflows.

## Acknowledgements

* [PyCryptodome Docs](https://pycryptodome.readthedocs.io)
* [OpenCV](https://opencv.org/)
* [Skimage](https://scikit-image.org/)
