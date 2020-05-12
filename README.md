# People-Counter-Application
In this project, i utilize the Intel® Distribution of the OpenVINO™ Toolkit to build a People Counter app, including performing inference on an input video, extracting and analyzing the output data, then sending that data to a server. These model was deployed on the edge, such that only data on 
1) the number of people in the frame,
2) time those people spent in frame, and 
3) the total number of people counted are sent to a MQTT server; inference will be done on the local machine.

# Resourses I Used:

A MQTT server - Which receives JSON from your primary code subsequent to inference concerning people counted, duration they spent in frame, and total people counted. This will feed to the UI server.

A UI server - displays a video feed as well as statistics received from the MQTT server.

A FFmpeg server - receives output image frames including any detected outputs inferred by the model. This is then fed to the UI server.

While the above files are provided complete so that no additional front-end or web services work is required from me.
Additionally,a video file to test my implementation, although my code allowed other inputs, such as a single image or webcam stream.

# IMPLEMENTATION, split into two files:

inference.py - Here, you will load the Intermediate Representation of the model, and work with the Inference Engine to actually perform inference on an input.
main.py - Here, you will:
Connect to the MQTT server
Handle the input stream
Use your work from inference.py to perform inference
Extract the model output, and draw any necessary information on the frame (bounding boxes, semantic masks, etc.)
Perform analysis on the output to determine the number of people in frame, time spent in frame, and the total number of people counted
Send statistics to the MQTT server
Send processed frame to FFmpeg



