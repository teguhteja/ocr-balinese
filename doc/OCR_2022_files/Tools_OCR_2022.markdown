# Tools OCR 2022
Created Sabtu 01 Januari 2022

Tesseract training font
-----------------------

1. <https://stackoverflow.com/questions/41295527/tesseract-training-for-a-new-font> — Tesseract training for a new font
2. <https://pretius.com/blog/ocr-tesseract-training-data/>
3. <https://stackoverflow.com/questions/57995023/train-tesseract-to-label-icons/58130617#58130617> — Train Tesseract to label icons
4. <https://medium.com/apegroup-texts/training-tesseract-for-labels-receipts-and-such-690f452e8f79> — 


Youtube OCR
-----------

1. <https://youtu.be/N5Y6gZgvryQ> — Tesseract OCR Training for New Fonts Language
2. <https://youtu.be/1v8BPw0Dn0I> — Tesseract OCR - Lesson 2: Training Tesseract for new font
3. <https://youtu.be/TpD76k2HYms>  — Training/Fine Tuning Tesseract OCR LSTM for New Fonts
4. <https://www.youtube.com/playlist?list=PLMtXi82tZQ3pir7F4gGL9fdf_9Oyrb9cH> — OCR Tessaract etc


GUI OCR
-------

1. gImageReader


Qt-Box-Editor
-------------

1. <https://github.com/zdenop/qt-box-editor>
2. <https://zdenop.github.io/qt-box-editor/>


### Build App

1. qmake > make


jTessBoxEditor
--------------

### Download jTessBoxEditor

1. <https://sourceforge.net/projects/vietocr/files/jTessBoxEditor/jTessBoxEditor-2.3.1.zip/download?css-reload=2>
2. <http://vietocr.sourceforge.net/training.html>
3. <https://sourceforge.net/p/vietocr/discussion/>


### Step jTessBoxEditor
jTessBox Editor:  <https://sourceforge.net/projects/viet>...

#### Step 1: Make box files for images that we want to train
Syntax: tesseract [langname].[fontname].[expN].[file-extension] [langname].[fontname].[expN] batch.nochop makebox
Eg:tesseract train.my.exp0.tif train.my.exp0 batch.nochop makebox

{*Note: After making box files we have to change or modify wrongly identified characters in box files.}

#### Step 2: Create .tr file
Create .tr file (Compounding image file and box file)
Syntax: tesseract [langname].[fontname].[expN].[file-extension] [langname].[fontname].[expN] box.train
Eg: tesseract train.my.exp.tif train.my.exp0 box.train

#### step 3: Extract the charset from the box files
Extract the charset from the box files (Output for this command is unicharset file)
Syntax: unicharset_extractor [langname].[fontname].[expN].box 
Eg: unicharset_extractor train.my.exp0.box

#### step 4: Create a font_properties file based on our needs.
Syntax: echo "[fontname] [italic (0 or 1)] [bold (0 or 1)] [monospace (0 or 1)] [serif (0 or 1)] [fraktur (0 or 1)]" [angle bracket should be here] font_properties 
Eg: echo "arial 0 0 1 0 0" [angled bracket] font_properties

#### Step 5: Training the data.
Syntax: mftraining -F font_properties -U unicharset -O [langname].unicharset [langname].[fontname].[expN].tr
Eg: mftraining -F font_properties -U unicharset -O train.unicharset train.my.exp0.tr

#### Step 6: training
Syntax: cntraining [langname].[fontname].[expN].tr
Eg: cntraining train.my.exp0.tr
{*Note:After step 5 and step 6 four files were created.(shapetable,inttemp,pffmtable,normproto) }

#### Step 7: Rename four files
Rename four files (shapetable,inttemp,pffmtable,normproto) into ([langname].shapetable,[langname].inttemp,[langname].pffmtable,[langname].normproto)
Syntax: rename filename1 filename2
Eg:
rename shapetable train.shapetable
rename inttemp train.inttemp
rename pffmtable train.pffmtable
rename normproto train.normproto


#### Step 8: Create .traineddata file
Syntax: combine_tessdata [langname].
Eg: combine_tessdata train.

Move .traineddata file to tesseract programs tessdata directory
C:\Program Files\Tesseract-OCR\tessdata

Run tesseract for trained fronts

tesseract Test2.png stdout -l train

Noto Sans Balinese
------------------

NTB
---

1. <https://fonts.google.com/noto/specimen/Noto+Sans> — download font
2. <https://r12a.github.io/scripts/balinese/>

```python
>>> A = "ᬕ᭄ᬢ"
>>> hex(ord(A[0]))
'0x1b15'
>>> hex(ord(A[1]))
'0x1b44'
>>> hex(ord(A[2]))
'0x1b22'
```
