# SiamFC - TensorFlow
TensorFlow port of the tracking method described in the paper [*Fully-Convolutional Siamese nets for object tracking*](https://www.robots.ox.ac.uk/~luca/siamese-fc.html).

In particular, it is the improved version presented as baseline in [*End-to-end representation learning for Correlation Filter based tracking*](https://www.robots.ox.ac.uk/~luca/cfnet.html), which achieves state-of-the-art performance at high framerate. The other methods presented in the paper (similar performance, shallower network) haven't been ported yet.



## Settings things up with virtualenv
1) Get virtualenv if you don't have it already
`pip install virtualenv`
1) Create new virtualenv with Python 2.7
`virtualenv --python=/usr/bin/python2.7 ve-tracking`
1) Activate the virtualenv
`source ~/tracking-ve/bin/activate`
1) Clone the repository
`git clone https://github.com/torrvision/siamfc-tf.git`
1) `cd siamfc-tf`
1) Install the required packages
`sudo pip install -r requirements.txt`
1) `mkdir pretrained data`
1) Download the [pretrained networks](https://bit.ly/cfnet_networks) in `pretrained` and unzip the archive (we will only use `baseline-conv5_e55.mat`)
1) Download [video sequences](https://drive.google.com/file/d/0B7Awq_aAemXQSnhBVW5LNmNvUU0/view) in `data` and unzip the archive.


## Running the tracker
1) Set `video` from `parameters.evaluation` to `"all"` or to a specific sequence (e.g. `"vot2016_ball1"`)
1) See if you are happy with the default parameters in `parameters/hyperparameters.json`
1) Optionally enable visualization in `parameters/run.json`
1) Call the main script (within an active virtualenv session)
`python run_tracker_evaluation.py`



# CFNet-Video-tracking-using-DPM
