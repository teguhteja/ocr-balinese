# Git OCR 2022
Created Sabtu 01 Januari 2022


1. <https://github.com/tesseract-ocr/langdata/issues/152> — 
	a. using jTessBoxEditor how to set Language 
	b. need font unicode => using Kadiri, Noto Sans Balinese, Noto Serif Balinese, Pustaka Bali, Vimala. The way tesseract (lstm version) works, the image will be recognised as Unicode text which will render correctly with Unicode Balinese fonts. So, both Vimala and Noto fonts should be able to render the same output.
	c. fine tuning <https://github.com/Shreeshrii/tesstrain-bali> 
	d. training => per line



2. <https://github.com/Shreeshrii/tesstrain-bali> — Finetune Training and OCR evaluation of Tesseract 5.0.0 Alpha for Balinese script using tesstrain Training workflow for Tesseract 4 as a Makefile.
	a. <https://github.com/Shreeshrii/tesstrain-bali/tree/master/gt/bali-Vimala>



3. <https://github.com/tesseract-ocr/langdata/issues/126> — 
	a. Collect training text in Javanese script (Unicode). You will need large number of lines, 500,000 or so to train from scratch. Or, if you can identify a current language/script supported by tesseract which is similar, then you can train by replacing layer, Try to get representative training text of about 50000 lines with 50 words each.
	b. Collect unicode fonts which can correctly render the above text. The more fonts you have the better it will be.
	c. Collect word frequency lists in Javanese script.
	d. Preferably use the linux platform for doing training.
	e. See <https://github.com/tesseract-ocr/tesseract/wiki/TrainingTesseract-4.00#training-just-a-few-layers>

	
You can try this as it will be faster than training from scratch.
Please post links to Javanese script related resources below.
If there is a transliterator which convertes Javanese in Latin script to Javanese script, that can be used for converting the files for lang jav as a start.


4. <https://github.com/gindrawan/balinese-script-training> — 

Image sources of the Balinese script recognition training:


