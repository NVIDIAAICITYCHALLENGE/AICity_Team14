AI CITY CHALLENGE TEAM 14 


SAN JOSE STATE UNIVERSITY

Folder structure

AICity_Team14 -> Detectnet -> code: Contains all the required Detectnet network files used in Digits front end tool for the model creation.

AICity_Team14 -> Detectnet -> code -> 14classes_aic_detectnet_deploy_network.prototxt: explains the Detectnet network with layers for 14 classes detection defined in the aic dataset.

AICity_Team14 -> Detectnet -> code -> bvlc_googlenet.caffemodel: pretrained model used for the training the aic dataset.

Detectnet trained model("snapshot_iter_74360.caffemodel") for 10 epochs is in the Detectnet folder - 
https://drive.google.com/open?id=0B7BvwOfVcWAKMzNVWktVc0VzQ1k

AICity_Team14 -> Darknet-> code: Contains entire Darknet framework code with all necessary changes required for AIC dataset aic1080 trained.

AICity_Team14 -> Darknet-> code -> cfg -> aic.data : contains the configurations and path locations for the training as well as validation folder of the dataset.

AICity_Team14 -> Darknet-> code -> cfg -> yolo-aic.cfg : explains the yolo network with layers defined for the aic dataset.

AICity_Team14 -> Darknet-> code -> data -> aic.names :contains all the 14 classes of the aic dataset which are to be detected.

Darknet trained model("Yolo-aic.backup") for 30000 iterations is in the Darknet folder - 
https://drive.google.com/open?id=0B7BvwOfVcWAKMzNVWktVc0VzQ1k

Execution of Detectnet model: 

Have just verified the Detectnet model using Digits GUI front end tool. So, no execution commands required.

Execution of Darknet model:

Command for training the model:
./darknet detector train cfg/aic.data cfg/yolo-aic.cfg

Command for testing the trained model:

Using the video file
./darknet detector demo cfg/aic.data cfg/yolo-aic.cfg yolo-aic.backup <video file>

Using the image file
./darknet detector test cfg/aic.data cfg/yolo-aic.cfg yolo-aic.backup <image file>






