# Motion Detection using Machine learning on Edge Impulse
The repo contains the implementation of a motion detection device that detects the up-down, right-left, circular and idel motion of the target machine i.e. mobile phone or any [supported board](https://docs.edgeimpulse.com/docs/development-platforms/fully-supported-development-boards)</br>
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
Head to the Impulse design page in your project. Add a <b>Spectral Analysis</b> processing block. Add a Classification-BrainChip Akida and a K-means Anomaly Detection block to the learning blocks section.
