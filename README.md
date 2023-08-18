# SurfaceDefectAI_Object_Detection_Approach_for_Industrial_Component_Inspection

         
Assembly line automation gets more significance to cope up with increasing needs of latest technology machines which are used in industry and society. This paper presents a computationally efficient 2D computer vision-based approach to recognize the machine parts and detect damaged parts on the assembly line. The image acquisition system which is part of the assembly line setup acquires data from the moving machine parts in line. Then a contour of the machine parts are extracted and normalized by equal part area method to describe the shape. It gives important clues for machine part shape recognition and defect identification.

For experimental purpose a model shape for each machine part is developed, the shape recognition and defect detection are performed with only reference to the model shape. The defects in the machine part such as damage, cracks are identified by the similarity measure between model shape and the data extracted from machine part of the assembly line. The detection and identification of defects at the early stage will helps smooth production process, saves production cost and time.

Surface defects are a major reason for poor quality of parts for manufacturers. Inspection processes done in industries are mostly manual and time consuming. To reduce error on identifying surface defects requires more automotive and accurate inspection process. Considering this lacking, this research implements a surface Defect Recognizer which uses computer vision methodology with the combination of local thresholding to identify possible defects. The recognizer identifies the surface defects within economical cost and produces less error prone inspection system in real time. In order to generate data set, primarily the recognizer captures digital gear images by image acquisition device. Later, the outputs of the processed image are the area of the faulty portion and compute the possible defective and non –defective surface image as an output.

 Subsequently, we discussed the types and characteristics of surface defect detection methods (conventional from industries as well as some advanced). Under the complex background of image acquisition, a new model faster r-CNN with TensorFlow is proposed for online detection of surface defects, and it was validated on our experimental platform for online flange yoke surface defect detection under a complex background. Results show that faster r-CNN with TensorFlow has better recognition of microdefects under a complex background than some other recognition networks. The proposed algorithm has good robustness as well.
            
# STEPS TO SET UP TENSORFLOW MODEL WITH FASTER R-CNN FOR OBJECT DETECTION:

Preparing the workspace – 

Installing tensorflow

Installing tensorflow object detection api

Importing pretrained model for faster r-cnn algorithm.

Install dependencies and compiling package.

# Preparing the dataset – 
  
# Annotate the dataset
Used labelimg (python based repoisitory ) for labelling the dataset
      
# Partition the dataset
Dividing the dataset into training and testing datasets with the 80/20 percent. i.e., 80 percent training dataset and remaining into test dataset for validation purpose.

# Create label map – 
TensorFlow requires a label map, which namely maps each of the used labels to an integer values. This label map is used both by the training and detection processes.

# Creating TFRecords –
Now that we have generated our annotations and split our dataset into the desired training and testing subsets, it is time to convert our annotations into the so called TFRecord format.

# Configuring a training job – 
Download pretrained model – 
Here we have taken faster r-cnn as a pretrained model.

# Training the model – 
Here we had started training of the model 
If everything has been set up correctly, TensorFlow will initialize the training. The initialization can take up to 30 seconds before the actual training begins.
Each step of training reports the loss. It will start high and get lower and lower as training progresses
 
# Exporting a trained model – 
Once your training job is complete, you need to extract the newly trained inference graph, which will be later used to perform the object detection. 
We can use this same inference graph as input to our prediction step with image acquisition system to get direct output within the seconds on production line itself as shown in figure 1 , we will get the signal output for defective parts detection and identification.


