# FusionNet

Please install tensorflow, keras, skimage, sklearn, opencv and related libraries using (sudo) pip install if you have the errors related with essential libraries.

Run mkdir models to save the checkpoint of model's weights

- Data.py read images and membrane labels from data folder
- Train.py train the model (define in Model.py) with data augmentation (Augment.py)
- Deploy_full.py predict the result (currently I predicted on the training set, you may set up 
- Utility.py includes all the needed libraries (sorry for my lazy mode). 

Update 15/05/2019 (Khoa)
- Fix the dependencies between Keras, tensorflow and others.
- Add fusion_net enviroment for running project. Just run this command in the project directory:\
 conda env create -f environment_FusionNet.yml
- There will be an error about :\
"File "/home/khoa/anaconda3/envs/fusion_net/lib/python2.7/site-packages/keras/backend/tensorflow_backend.py", line 683, in normalize_batch_in_training
    target_shape = tf.pack(target_shape)
AttributeError: 'module' object has no attribute 'pack'"/
Then go to "tensorflow_backend.py" and change :\
target_shape = tf.pack(target_shape) => target_shape = tf.stack(target_shape)


