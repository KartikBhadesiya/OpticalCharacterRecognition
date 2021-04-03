# OpticalCharacterRecognition
OpenCV package is used to read an image and perform certain image processing techniques. Python-tesseract is a wrapper for Google’s Tesseract-OCR Engine which is used to recognize text from images.

Steps:
1. Import required packages
2. Mention the installed location of Tesseract-OCR in your system
3. Read image from which text needs to be extracted
4. Convert the image to gray scale
5. Performing OTSU threshold or we can use any other thresholding methods like adaptive thresholding, binary thresholding
6. Select a rectangular kernel for selecting text from an image
7. Apply Dilation
8. Find Contours
9. Create a copy of the image so that it does not override the image
10. Loop over the contours drawing rectangle on the text, cropping the image, opening a file to save the image, applying tesseract to the image, writing text to the image and closing the file. 

# To Install Tesseract on Windows
1. Install tesseract using windows installer available at: https://github.com/UB-Mannheim/tesseract/wiki

2. Note the tesseract path from the installation. Default installation path at the time of this edit was: C:\Users\USER\AppData\Local\Tesseract-OCR. It may change so please check the installation path.

3. pip install pytesseract

4. Set the tesseract path in the script before calling image_to_string:

pytesseract.pytesseract.tesseract_cmd = r'C:\Users\USER\AppData\Local\Tesseract-OCR\tesseract.exe'
