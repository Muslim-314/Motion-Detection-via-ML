# Motion Detection using Machine learning on Edge Impulse
The repo contains the implementation of a motion detection device that detects the up-down, right-left, circular and idle motion of the target machine i.e. mobile phone or any [supported board](https://docs.edgeimpulse.com/docs/development-platforms/fully-supported-development-boards)</br>
## Data Collection
Connect your phone to the Edge Impulse platform
![](images/connect.png)
once your phone is connected start collecting by clicking starting recording on your phone
<p float="left">
  <img src="images/phone-con.jpg"  width="30%" />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="images/data-col.jpg"     width="30%" />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="images/sampling.jpg"  width="30%" />
</p>

Now shake your phone right-left 10 to 20 times and do the same for up-down and circular motion. For idleness leave your phone and on a plane desk and then record.
Your data will appear in the Data Acquisition section don't forget to label your data.

![](images/collected.png)
## Feature Extraction
Head to the Impulse design page in your project. Add a <b>Spectral Analysis</b> processing block. Add a <b>Classification-BrainChip Akida</b> and a <b>K-means Anomaly Detection</b> block to the learning blocks section.
![](images/FE.png)
After saving impulse head on to the spectral features and generate features.
![](images/GF.png)
## Model Training
Head to the <b>Classification-BrainChip Akida</b> page in your project. Click Start Training. After a few minutes, the model should be done training. Now you can monitor the accuracy of the Model<be>
<p align="center">
    <img  src="images/model.png">
</p>
Now go to the Anomaly detection page and select the features to train. I have selected RMS values of acceleration along the x, y, and z axis.

<p float="left">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="images/I2.png"  width="40%" />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="images/I1.png"     width="50%" />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</p>

## Model Deployment
Go to the <b>Deployment Page</b> and Scan the <b>QR code<b> using your phone.<be>

<p align="center">
    <img  src="images/Deployment.jpg"width="40%" >
</p>
The model predicts the probability of the state of the device. If the device is idle the probability of idle will be one and same goes for the up-down, right-left and circular motion.
