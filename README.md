AI CITY CHALLENGE TEAM 14 


SAN JOSE STATE UNIVERSITY

Clone the complete  "master" repository.

Folder structure

Detectnet Procedure:

AICity_Team14 -> Detectnet -> code: Contains all the required Detectnet network files used in Digits front end tool for the model creation.

AICity_Team14 -> Detectnet -> code -> 14classes_aic_detectnet_deploy_network.prototxt: explains the Detectnet network with layers for 14 classes detection defined in the aic dataset.

AICity_Team14 -> Detectnet -> code -> bvlc_googlenet.caffemodel: pretrained model used for the training the aic dataset.

Detectnet trained model("snapshot_iter_74360.caffemodel") for 10 epochs is in the Detectnet folder - 
https://drive.google.com/open?id=0B7BvwOfVcWAKMzNVWktVc0VzQ1k

Darknet Procedure:

AICity_Team14 -> Darknet-> code: Contains entire Darknet framework code with all necessary changes required for AIC dataset aic1080 trained.

Please download the cfg folder from -
https://drive.google.com/open?id=0B7BvwOfVcWAKMzNVWktVc0VzQ1k and place it inside "<path>\AICity_Team14\Darknet\code" as shown below.

AICity_Team14 -> Darknet-> code -> cfg -> aic.data : contains the configurations and path locations for the training as well as validation folder of the dataset.

AICity_Team14 -> Darknet-> code -> cfg -> yolo-aic.cfg : explains the yolo network with layers defined for the aic dataset.

Please download the data folder from -
https://drive.google.com/open?id=0B7BvwOfVcWAKMzNVWktVc0VzQ1k and place it inside "<path>\AICity_Team14\Darknet\code" as shown below.

AICity_Team14 -> Darknet-> code -> data -> aic.names :contains all the 14 classes of the aic dataset which are to be detected.

Darknet trained model("Yolo-aic.backup") for 30000 iterations is in the Darknet folder - 
https://drive.google.com/open?id=0B7BvwOfVcWAKMzNVWktVc0VzQ1k and place it indise -> "<path>\AICity_Team14\Darknet\model"

Execution of Detectnet model: 

We have ave just verified the Detectnet model using Digits GUI front end tool. So, no execution commands required.

Execution of Darknet model:

Open a command prompt terminal and change the directory to "<path>\AICity_Team14\Darknet\code"

Command for training the model:
./darknet detector train cfg/aic.data cfg/yolo-aic.cfg

Command for testing the trained model:

Using the video file
./darknet detector demo cfg/aic.data cfg/yolo-aic.cfg <path>\AICity_Team14\Darknet\model\yolo-aic.backup <video file>

Using the image file
./darknet detector test cfg/aic.data cfg/yolo-aic.cfg <path>\AICity_Team14\Darknet\model\yolo-aic.backup <image file>
