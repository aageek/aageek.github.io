
Installation of CUDA® Toolkit  & cuDNN 
and make sure you have them in enviromental variable   

Cuda  : https://developer.nvidia.com/cuda-90-download-archive
* cuda_9.0.176_win10.exe
```
$ nvcc --version

nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2017 NVIDIA Corporation
Built on Fri_Sep__1_21:08:32_Central_Daylight_Time_2017
Cuda compilation tools, release 9.0, V9.0.176

```

cuDNN : https://developer.nvidia.com/cudnn 

```
$ where cudnn*
C:\cuda\bin\cudnn64_7.dll

PS C:\> type "C:\cuda\include\cudnn.h" | findstr CUDNN_MAJOR
#define CUDNN_MAJOR 7
#define CUDNN_VERSION    (CUDNN_MAJOR * 1000 + CUDNN_MINOR * 100 + CUDNN_PATCHLEVEL)
PS C:\Users\abhanand>
```

Environment Variable 
```
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\bin
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\libnvvp
C:\cuda\bin
```


$ conda create --name tensorflowgpu pip python=3.6
```
Solving environment: done

## Package Plan ##

  environment location: C:\anaconda3\envs\tensorflowgpu

  added / updated specs:
    - pip
    - python=3.6


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    wheel-0.31.1               |           py36_0          79 KB  conda-forge
    vs2015_runtime-14.0.25420  |                0         1.9 MB  conda-forge
    python-3.6.5               |                1        19.5 MB  conda-forge
    setuptools-40.0.0          |           py36_0         568 KB  conda-forge
    pip-9.0.3                  |           py36_0         1.8 MB  conda-forge
    wincertstore-0.2           |           py36_1          13 KB  conda-forge
    ------------------------------------------------------------
                                           Total:        23.8 MB

The following NEW packages will be INSTALLED:

    certifi:        2018.4.16-py36_0 conda-forge
    pip:            9.0.3-py36_0     conda-forge
    python:         3.6.5-1          conda-forge
    setuptools:     40.0.0-py36_0    conda-forge
    vs2015_runtime: 14.0.25420-0     conda-forge
    wheel:          0.31.1-py36_0    conda-forge
    wincertstore:   0.2-py36_1       conda-forge

Proceed ([y]/n)? y


Downloading and Extracting Packages
wheel-0.31.1         |   79 KB | ##################################################################################################################################################################################################################################### | 100%
vs2015_runtime-14.0. |  1.9 MB | ##################################################################################################################################################################################################################################### | 100%
python-3.6.5         | 19.5 MB | ##################################################################################################################################################################################################################################### | 100%
setuptools-40.0.0    |  568 KB | ##################################################################################################################################################################################################################################### | 100%
pip-9.0.3            |  1.8 MB | ##################################################################################################################################################################################################################################### | 100%
wincertstore-0.2     |   13 KB | ##################################################################################################################################################################################################################################### | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use:
# > activate tensorflowgpu
#
# To deactivate an active environment, use:
# > deactivate
#
# * for power-users using bash, you must source
#

```
$ source activate tensorflowgpu
(tensorflowgpu)
$ pip install --ignore-installed --upgrade tensorflow-gpu
```
Collecting tensorflow-gpu
  Downloading https://files.pythonhosted.org/packages/51/bc/29202147b513f0ed5fbdd40f05c6bc2a19722cfb4dd24d77a7c2080a06b4/tensorflow_gpu-1.9.0-cp36-cp36m-win_amd64.whl (103.3MB)
    100% |████████████████████████████████| 103.3MB 11kB/s
Collecting wheel>=0.26 (from tensorflow-gpu)
  Using cached https://files.pythonhosted.org/packages/81/30/e935244ca6165187ae8be876b6316ae201b71485538ffac1d718843025a9/wheel-0.31.1-py2.py3-none-any.whl
Collecting grpcio>=1.8.6 (from tensorflow-gpu)
  Using cached https://files.pythonhosted.org/packages/d5/c6/15728549704f9c03db7179b7f99303b91b7703e18a50f5e7b47e59b289ea/grpcio-1.13.0-cp36-cp36m-win_amd64.whlCollecting gast>=0.2.0 (from tensorflow-gpu)
Collecting numpy>=1.13.3 (from tensorflow-gpu)
  Using cached https://files.pythonhosted.org/packages/0d/b7/0c804e0bcba6505f8392d042d5e333a5e06f308e019517111fbc7767a0bc/numpy-1.14.5-cp36-none-win_amd64.whl
Collecting six>=1.10.0 (from tensorflow-gpu)  Using cached https://files.pythonhosted.org/packages/67/4b/141a581104b1f6397bfa78ac9d43d8ad29a7ca43ea90a2d863fe3056e86a/six-1.11.0-py2.py3-none-any.whl
Collecting setuptools<=39.1.0 (from tensorflow-gpu)
  Using cached https://files.pythonhosted.org/packages/8c/10/79282747f9169f21c053c562a0baa21815a8c7879be97abd930dbcf862e8/setuptools-39.1.0-py2.py3-none-any.whlCollecting absl-py>=0.1.6 (from tensorflow-gpu)
Collecting protobuf>=3.4.0 (from tensorflow-gpu)
  Using cached https://files.pythonhosted.org/packages/75/7a/0dba607e50b97f6a89fa3f96e23bf56922fa59d748238b30507bfe361bbc/protobuf-3.6.0-cp36-cp36m-win_amd64.whlCollecting termcolor>=1.1.0 (from tensorflow-gpu)
Collecting astor>=0.6.0 (from tensorflow-gpu)
  Using cached https://files.pythonhosted.org/packages/35/6b/11530768cac581a12952a2aad00e1526b89d242d0b9f59534ef6e6a1752f/astor-0.7.1-py2.py3-none-any.whl
Collecting tensorboard<1.10.0,>=1.9.0 (from tensorflow-gpu)  Using cached https://files.pythonhosted.org/packages/9e/1f/3da43860db614e294a034e42d4be5c8f7f0d2c75dc1c428c541116d8cdab/tensorboard-1.9.0-py3-none-any.whl
Collecting markdown>=2.6.8 (from tensorboard<1.10.0,>=1.9.0->tensorflow-gpu)
  Using cached https://files.pythonhosted.org/packages/6d/7d/488b90f470b96531a3f5788cf12a93332f543dbab13c423a5e7ce96a0493/Markdown-2.6.11-py2.py3-none-any.whl
Collecting werkzeug>=0.11.10 (from tensorboard<1.10.0,>=1.9.0->tensorflow-gpu)  Using cached https://files.pythonhosted.org/packages/20/c4/12e3e56473e52375aa29c4764e70d1b8f3efa6682bef8d0aae04fe335243/Werkzeug-0.14.1-py2.py3-none-any.whl
Installing collected packages: wheel, six, grpcio, gast, numpy, setuptools, absl-py, protobuf, termcolor, astor, markdown, werkzeug, tensorboard, tensorflow-gpu
Successfully installed absl-py-0.2.2 astor-0.7.1 gast-0.2.0 grpcio-1.13.0 markdown-2.6.11 numpy-1.14.5 protobuf-3.6.0 setuptools-40.0.0 six-1.11.0 tensorboard-1.9.0 tensorflow-gpu-1.9.0 termcolor-1.1.0 werkzeug-0.14.1 wheel-0.31.1
You are using pip version 9.0.3, however version 10.0.1 is available.
You should consider upgrading via the 'python -m pip install --upgrade pip' command.(tensorflowgpu)

```

abhanand@AAHP MINGW64 ~/Documents/azml
$ source activate tensorflowgpu
(tensorflowgpu)
abhanand@AAHP MINGW64 ~/Documents/azml
$ python
```
Python 3.6.5 | packaged by conda-forge | (default, Apr  6 2018, 16:13:55) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import tensorflow as tf
>>> hello = tf.constant('Hello, TensorFlow!')
>>> sess = tf.Session()
2018-07-13 09:37:10.114383: I T:\src\github\tensorflow\tensorflow\core\platform\cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2
2018-07-13 09:37:10.743058: I T:\src\github\tensorflow\tensorflow\core\common_runtime\gpu\gpu_device.cc:1392] Found device 0 with properties:
name: Quadro K420 major: 3 minor: 0 memoryClockRate(GHz): 0.8755
pciBusID: 0000:04:00.0
totalMemory: 2.00GiB freeMemory: 1.67GiB
2018-07-13 09:37:10.755052: I T:\src\github\tensorflow\tensorflow\core\common_runtime\gpu\gpu_device.cc:1471] Adding visible gpu devices: 0
2018-07-13 09:37:11.220379: I T:\src\github\tensorflow\tensorflow\core\common_runtime\gpu\gpu_device.cc:952] Device interconnect StreamExecutor with strength 1 edge matrix:
2018-07-13 09:37:11.227111: I T:\src\github\tensorflow\tensorflow\core\common_runtime\gpu\gpu_device.cc:958]      0
2018-07-13 09:37:11.231459: I T:\src\github\tensorflow\tensorflow\core\common_runtime\gpu\gpu_device.cc:971] 0:   N
2018-07-13 09:37:11.237243: I T:\src\github\tensorflow\tensorflow\core\common_runtime\gpu\gpu_device.cc:1084] Created TensorFlow device (/job:localhost/replica:0/task:0/device:GPU:0 with 1448 MB memory) -> physical GPU (device: 0, name: Quadro K420, pci bus id: 0000:04:00.0, compute capability: 3.0)
>>> print(sess.run(hello))
b'Hello, TensorFlow!'
>>>
```