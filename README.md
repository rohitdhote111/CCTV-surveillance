# Deep Learning based CCTV surveillance
  Intelligent surveillance system at Stone crusher site for counting Number of Trucks unloading at stone crusher.
Previously a civil contractor use to pay to the labourers 4500 rupees per truck for unloading at the inlet of 
stone crusher and complete payable amount was calculated based on manual supervision with the help of CCTV surveillance.
but this method has several drawbacks as follows:
1. During manual supervision of CCTV footage (considering working time of site from 8 AM to 6 PM)daily about 10 hrs of data generated.
   To supervise this manually maximum fast forwarding speed is 4X so still 10/4 = 2.5 hrs are required to supervise daily generated data.
2. Manual supervision requires additional trustworthy human worker.
3. corrupt supervisor can cause loss of thousands of rupees to the contractor.


I have provided here a Neural Network approach for this problem. The problem is considered as a classification problem where 
If the truck is present in the Image then classify it as 1 
If the truck is NOT present in the Image then classify it as 0

# Methodology :

  ## Preparation of Dataset :
   1. collection : Uniformly distributed video footage was collected from various seasonal conditions(summer, winter, Monsoon).
                    Data also consists of various light conditions as per daily variation(Morning, afternoon, evening).
                    
   Using functions of openCV library images are extrected from videos and cropped as per requirement.
                    
   2. Labelling : According to the presence and absence of trucks in the cropped images data is stored in two separate folders.
                   Folders are labelled as 0 and 1. and  complete data is split into train test set.
                   Train Data = 479 images (80 %)
                   Test Data = 119 imgages (20 %)
  
  ## Training of Model:
   1. For traning purpose google colab is used and complete data is uploaded on Google drive for smooth importing of data.
   2. Using Keras Preprocessing tools data is imported in google colab.
   3. after batch Normalization and autotuning of data Sequential model was used in KERAS framework.
   4. Model consists of Maxpooling and Relu actvation function.
   5. For compiling Adam optimizer was used.
    
    
    Validation accuracy of 96.64% was achieved on the model.
                    
