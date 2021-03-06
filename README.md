# Introduction to Cultural Data Science - final project
Code and data for my CDS final project

### MIT License

Copyright (c) 2020 Sophia Kleist Karlson

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


### Please run the code in the following order:

1. Download the data (the ZIP-file, three CSV-files and folder with source drawings).

2. Run Image_preprocessing_script in your browser (in Google Colaboratory).

3. Download R_preprocessing_and_plotting and run it locally on your computer (in RStudio).

NB: Remember to change the working directory and pathds to the CSV's where necessary to fit your own folder structure.


### Data metadata 
Written in the format "column name": "description". If a column name appears in more than one CSV-file, they describe the same variable.

Subject: Anonymized participant identifier, unique to each participant.

Chain: Chain ID. Note that 25 chains were started, but chains 1, 6, 10, 11 and 24 were excluded due to missing data. This means that there are 20 chain ID's present in this dataset with ID's ranging 0-23.

Generation: Generation ID. Note that in the file cleaned_data_small.csv, generation ranges from 0-6, whereas it ranges from 0-7 in the final dataset, as all generations were pushed one up to make the source images the new "generation 0" for each chain. 

Condition: The condition (1-4) that the drawing of that row was a assigned.

Source_image: Which of the 12 soure drawings was this drawing originally copied from at the beginning of the chain. Ranges 1-12.

files.image.path: Path to the drawings as they are placed within the ZIP-file with the drawings and JSON session data (the JSON files are not published here as they contain personal data from the participants).

Drawing_ID: Unique drawing identifier. For the drawings produced by the participant, this ID contains information about the chain, generation, condition and source drawing of the drawing (e.g. "Chain_7_Gen_2_Cond_1_Source_12"). For the source drawings, the drawing ID takes the format "stim_x" where x is a number between 1 and 12.

Complexity_orignal: Algorithmic complexity of a drawing, measured as the filesize in bytes of the image converted into JPEG2000 format. This score is the complexity calculated from the original (resized) drawing before blurring it.

Complexity: Algorithmic complexity of a drawing, measured as the filesize in bytes of the image converted into JPEG2000 format. This score is the complexity calculated after the resized image has been blurred.

Conventionality: Score of how "conventionally recognizable" the drawing is perceived to be, e.g. if different people would agree on what the drawing represents. The scale ranges from 0-10, where 0 means "0 % conventional" and 10 means "100 % conventional".
