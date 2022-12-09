# Ml-for-Cybersecurity   
├── data 

    └── cl
        └── valid.h5 // this is clean validation data used to design the defense
        └── test.h5  // this is clean test data used to evaluate the BadNet
    └── bd
        └── bd_valid.h5 // this is sunglasses poisoned validation data
        └── bd_test.h5  // this is sunglasses poisoned test data
├── models

    └── bd_net.h5
    └── bd_weights.h5
## 1.Dependencies
  1.Python 3.6.9  
  2.Keras 2.3.1  
  3.Numpy 1.16.3  
  4.Matplotlib 2.2.2   
  5.H5py 2.9.0   
  6.TensorFlow-gpu 1.15.2   
  
## 2.Data   
 1.Download the validation and test datasets from https://drive.google.com/drive/folders/1U7izqIiyud6gCkDcu5G2JZY2ZWNR2O8x?usp=share_link and store them under data/ directory.     
 2.The dataset contains images from YouTube Aligned Face Dataset. We retrieve 1283 individuals and split into validation and test datasets.   
 
 ## 3.Evaluating the Backdoored Model
The DNN architecture used to train the face recognition model is the state-of-the-art DeepID network.     

To evaluate the backdoored model, execute eval.py by running:  
    python3 eval.py clean validation data directory poisoned validation data directory model directory.      
