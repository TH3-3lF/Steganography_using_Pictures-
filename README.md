# Steganography using Pictures

A simple Python-based steganography tool that hides secret text messages within image files using OpenCV. This tool allows you to encode messages into images and decode them back with password protection.

## Features

- **Text Encoding**: Hide secret messages within image pixels
- **Password Protection**: Secure your hidden messages with a passcode
- **Image Processing**: Uses OpenCV for image manipulation
- **Cross-platform**: Works on Windows, macOS, and Linux
- **Simple Interface**: Command-line interface for easy usage

## Requirements

- Python 3.x
- OpenCV (`cv2`)
- An image file (the repository includes `Image_1.jpg` and `Image_2.jpg` as samples)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/TH3-3lF/Steganography_using_Pictures-.git
cd Steganography_using_Pictures-
```

2. Install required dependencies:
```bash
pip install opencv-python
```

## Usage

1. Place your target image in the project directory (you can use the provided `Image_1.jpg` or `Image_2.jpg`, or add your own)

2. Update the image path in `stego.py` if using a different image

3. Run the script:
```bash
python stego.py
```

3. Follow the prompts:
   - Enter your secret message
   - Set a passcode for protection
   - The tool will create an `encryptedImage.jpg` file with your hidden message

4. To decrypt:
   - Run the script again
   - Enter the correct passcode when prompted
   - Your hidden message will be revealed

## How It Works

The tool uses a simple steganography technique:

1. **Encoding**: Each character of the secret message is converted to its ASCII value and stored in the RGB channels of image pixels
2. **Pixel Traversal**: The algorithm moves through pixels in a diagonal pattern (incrementing row, column, and cycling through RGB channels)
3. **Password Protection**: A passcode is required to decrypt the hidden message
4. **Decoding**: The process is reversed to extract the original message from the modified image

## Code Structure

- **Dictionary Creation**: Maps characters to ASCII values and vice versa
- **Message Encoding**: Embeds message characters into image pixels
- **Image Saving**: Saves the modified image with hidden data
- **Message Decoding**: Extracts and reconstructs the original message
- **Password Verification**: Ensures only authorized users can decrypt messages

## Example

```
Enter secret message: Hello World!
Enter a passcode: mypassword123

# Image processing occurs...
# encryptedImage.jpg is created

Enter passcode for Decryption: mypassword123
Decryption message: Hello World!
```

## Important Notes

⚠️ **Security Considerations**:
- This is a basic implementation for educational purposes
- The password protection is simple and not cryptographically secure
- For production use, consider implementing proper encryption algorithms

⚠️ **Limitations**:
- Message length is limited by image size
- Only works with specific image formats
- No error handling for invalid inputs or corrupted images
k the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Potential Improvements

- Add support for multiple image formats
- Implement stronger encryption methods
- Add error handling and input validation
- Create a GUI interface
- Support for longer messages
- Image compression resistance

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This tool is for educational purposes only. Users are responsible for ensuring they comply with all applicable laws and regulations when using steganography tools.

## Author

Your Name - [your.email@example.com](mailto:your.email@example.com)

Project Link: [https://github.com/TH3-3lF/Steganography_using_Pictures-](https://github.com/TH3-3lF/Steganography_using_Pictures-)
