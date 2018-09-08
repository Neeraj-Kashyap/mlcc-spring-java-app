# TensorFlow Java application with Spring Framework and Gradle for Google MLCC
Object detection server side application sample program written in Java to teach Tensorflow and ML app dev. It uses the TensorFlow Java API with a trained YOLOv2 model. The server application is implemented with Spring boot Framework and it is built by Gradle.


This application is built on the top of application from https://github.com/szaza .
I have added my modifications to the same
#### How it works?

It provides a web user interface to upload images and detect objects.

#### Compile and run

Preconditions:
- Java JDK 1.8 or greater;
- TensorFlow 1.6 or grater;
- Git version control system;

Strongly recommended to install:
- nVidia CUDA Toolkit 8.0 or higher version;
- nVidia cuDNN GPU accelerated deep learning framework;

**Download the frozen graph and the label file**

Before compiling the source code you have to place the frozen graph and the label file into the `./graph/YOLO` directory. Download one of my graphs from my [google drive](https://drive.google.com/drive/folders/1GfS1Yle7Xari1tRUEi2EDYedFteAOaoN). There are two graphs: tiny-yolo-voc.pb and yolo-voc.pb. The tiny-yolo.pb has a lower size, however it is less accurate than the yolo-voc.pb. Modify the [application.yml](https://github.com/szaza/tensorflow-java-examples-spring/blob/master/src/main/resources/application.yml) configuration file if it is necessary. Here you can increase the file upload limit also.

**Compile with Gradle**

Compile the code by typing `./gradlew clean build` in the terminal window.<br/>
Run it with the command `./gradlew bootRun`

Open the [http://localhost:8080](http://localhost:8080) and you should see the webpage.<br/>

