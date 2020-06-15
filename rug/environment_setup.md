## Description of setting up a Peregrine GPU node to run the code
Unfortunately, creating a conda environment as described in the root README was not succesful. I followed the steps below to set up an environment anyway.

First login through SSH.

Loading Anaconda.

```
$ module load Anaconda3
```

Creating a conda environment.

```
$ conda create --name tbad_test4
```

Activating the environment (this might require some setup of conda).

```
$ conda activate tbad_test4
```

Some conda-based packages.

```
(tbad_test4) $ module load TensorFlow/1.8.0-fosscuda-2018a-Python-3.6.4
(tbad_test4) $ module load OpenCV/3.4.1-foss-2018a-Python-3.6.4
```

What's left is installing the required packages through pip. This only needs be done once.

```
pip install --user tensorflow==1.8.0
pip install --user keras==2.1.6
pip install --user scikit-image==0.14.0
pip install --user scikit-image==0.14.0
pip install --user scikit-learn==0.20.0
```

Copying in the dataset (link in the root README). From your local machine:

```
$ scp data.zip <username>@pg-gpu.hpc.rug.nl:tbad/skeleton_based_anomaly_detection/
```

(Log in with SSH)

```
$ cd tbad/skeleton_based_anomaly_detection
$ unzip data.zip
```
