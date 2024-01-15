# Automatic Number Plate Detector and Logger through Live Webcam

## Project Work Flow

1. Install and setup
2. Getting Licence plate data
3. Training a OD Model
4. Detecting Licence Plates
5. Applying OCR to Text
6. Output ROIs and Results

## Working

there are two key libraries used:
1. Object detection to find region of interest
2. Easy OCR to extract the text

## Functioning

1. real-time webcam feed grabs image of the plate
2. tensorflow object detection will detect the plate trained on kaggle dataset
3. used easy OCR to extract text and leverage a size filtering algorithm to grab the largestdetection region

## Steps
<br />
<b>Step 1.</b> Clone this repository: 
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv anprsys
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source anprsys/bin/activate # Linux
.\anprsys\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=anprsys
</pre>
<br/>

<b>Step 5.</b> 
run the `2. Training and Detection notebook` to set up the folder structure
<br/>

<b>Step 6.</b> 
Download the kaggle's car plate detection dataset, in /Tensorflow/workspace/images and split images and annotation in train and test set
<br/>


## Training the object detection model
1. Update Labels -> we have got only one i.e licence in annotations
2. Create TF Records -> the file formats the the object dection model requires fo the data to be in
3. Prepare Configuration
4. Train