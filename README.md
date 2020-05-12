# People-Counter-Application
In this project, i utilize the Intel® Distribution of the OpenVINO™ Toolkit to build a People Counter app, including performing inference on an input video, extracting and analyzing the output data, then sending that data to a server. These model was deployed on the edge, such that only data on 
1) the number of people in the frame,
2) time those people spent in frame, and 
3) the total number of people counted are sent to a MQTT server; inference will be done on the local machine.

# Resourses I Used:

A MQTT server - Which receives JSON from your primary code subsequent to inference concerning people counted, duration they spent in frame, and total people counted. This will feed to the UI server.

A UI server - displays a video feed as well as statistics received from the MQTT server.

A FFmpeg server - receives output image frames including any detected outputs inferred by the model. This is then fed to the UI server.

While the above files are provided complete so that no additional front-end or web services work is required from you, feel free to adjust these as you see fit.
Additionally, I provided  a video file to test your implementation, although your code should allow for other inputs, such as a single image or webcam stream.


