# Mined and Unmined Areas Detection. The Walkthrough
<p>This set of Notebooks provides a complete set of code to be able to train and leverage your own custom object detection model using the Tensorflow Object Detection API. 
<img src="https://user-images.githubusercontent.com/38394300/194756817-53ebbb4f-407c-43ab-84bf-497535eca636.JPG">
<img src="https://user-images.githubusercontent.com/38394300/194757687-cb879168-fa57-41ed-9425-c11eabf1b24c.JPG">
<img src="https://user-images.githubusercontent.com/38394300/194758376-0eae3770-f72a-48b7-8a9f-5a84c6e9efc8.jpg">

## Steps
<br />
<b>Step 1.</b> Clone this repository:  https://github.com/Dex247/Mined-and-Unmined-Areas-Detection-Using-The-Drone
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv tfod
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<img src="https://user-images.githubusercontent.com/38394300/194757548-a9239aff-42cc-48c3-8aff-eb25bda8b4ef.JPG">
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfodj
</pre>
<br/>
<b>Step 5.</b> Collect images using the Notebook - ensure you change the kernel to the virtual environment as shown below
<img src="https://i.imgur.com/8yac6Xl.png"> 
<br/>
<b>Step 6.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
\TFODCourse\Tensorflow\workspace\images\train<br />
\TFODCourse\Tensorflow\workspace\images\test
<img src="https://user-images.githubusercontent.com/38394300/194761743-fc905ed0-f42c-49ea-8ab5-8215c3216cb6.JPG">
<br/><br/>
<b>Step 7.</b> Begin training process >2. Training and Detection.ipynb</a>, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 8.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
<img src="https://i.imgur.com/FSQFo16.png">
If not, resolve installation errors by referring to the <a href="https://https://github.com/Dex247/Mined-and-Unmined-Areas-Detection-Using-The-Drone/main/README.md">Error Guide.md</a> in this folder.
<br /> <br/>
<b>Step 9.</b> Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 
<img src="https://user-images.githubusercontent.com/38394300/194758685-0f557bb6-f61c-4e4f-8833-4d9d282dfad4.JPG"> 
<img src="https://user-images.githubusercontent.com/38394300/194758847-a4365a25-0cb9-41cd-8f06-075fa9efdb2d.JPG">

<br />
<b>Step 10.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<img src="https://user-images.githubusercontent.com/38394300/194759175-80e032a1-1adf-4fe2-80a8-0bdfa31069ff.JPG">
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. </pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
<br />
<img src="https://user-images.githubusercontent.com/38394300/194761611-9a96bed9-a8b1-41ff-82a8-608bb090fd39.JPG">
