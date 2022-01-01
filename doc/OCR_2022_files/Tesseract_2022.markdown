# Tesseract 2022
Sen 27 Des 2021 10:05:27 

langdata
--------
Source training data for Tesseract for lots of languages
Want to re-train tesseract for a specific language, by modifying/augmenting the original training data? Then you have come to the right place!
If you want to find a language data set to run Tesseract, then look at our tessdata repository [<https://github.com/tesseract-ocr/tessdata>] instead.
To re-create the training of a single language, lang, you need the following:
All the data in the lang directory.
The corresponding unicharset/xheights files for the script(s) used by lang.
All the remaining non-lang-specific files in the top-level directory, such as font_properties.
You also need to obtain the fonts needed to train the language. Some languages were trained with commercially available fonts, so you will need to buy them in order to reproduce the training exactly, or use substitutes.


tesstrain
---------
Training workflow for Tesseract 4 as a Makefile for dependency tracking and building the required software from source.

Install Tesseract
-----------------
<https://ubuntuhandbook.org/index.php/2021/12/install-tesseract-ocr-5-ubuntu/>

<https://github.com/bhadreshpsavani/OCR_using_TesseatactLib_Project/blob/master/OCRusingTesseract.ipynb>
<https://nanonets.com/blog/ocr-with-tesseract/#preprocessingfortesseract>
<https://www.learnopencv.com/deep-learning-based-text-recognition-ocr-using-tesseract-and-opencv/>
<https://github.com/tesseract-ocr/tesseract>
<https://medium.com/milooproject/membuat-optical-character-recognition-ocr-sederhana-menggunakan-python-1fad7d427447>
<https://towardsdatascience.com/create-simple-optical-character-recognition-ocr-with-python-6d90adb82bb8>
<https://medium.com/@fahmisalman/an-easy-way-of-creating-text-localization-and-detection-in-tesseract-ocr-24cc89ed6fbc>
<https://www.pyimagesearch.com/2018/09/17/opencv-ocr-and-text-recognition-with-tesseract/>	
<https://www.pyimagesearch.com/2017/07/10/using-tesseract-ocr-python/>
<https://www.thepythoncode.com/article/optical-character-recognition-pytesseract-python>


LSTM
----
<http://colah.github.io/posts/2015-08-Understanding-LSTMs/>

git
---
[OpenCV]()
<https://www.coursera.org/projects/ocr-text-detection-tensorflow-opencv-tesseract>


TensorFlow
----------
<https://www.tensorflow.org/hub/>
<https://www.tensorflow.org/hub/tutorials>

Tesseract 4 & 5
---------------
Tesseract 4.0 added a new OCR engine based on LSTM neural networks. It works well on x86/Linux with official Language Model data available for 100+ languages and 35+ scripts. See 4.0x-Changelog for more details.

Tesseract 5.0.0.x source code is available in the main branch of the repository. The main branch is using 5.0.0 versioning because C++ code modernization caused API incompatibility with 4.x release.

for different verion tesseract 4 using appimage and tesseract 5 using command line

