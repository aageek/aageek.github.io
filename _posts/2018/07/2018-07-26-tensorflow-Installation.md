---
layout: post
title:  "Tensorflow installation with Anaconda on MacOS"
date:   2018-07-26
categories: post
---

### Tensorflow installation with Anaconda on MacOS

(My Machine Configuration)

```
$ system_profiler SPSoftwareDataType
Software:

    System Software Overview:

      System Version: macOS 10.13.5 (17F77)
      Kernel Version: Darwin 17.6.0
      Boot Volume: Macintosh HD
      Boot Mode: Normal
      Computer Name: XXXXXXXXXX
      User Name: XXXXXXXXXX
      Secure Virtual Memory: Enabled
      System Integrity Protection: Enabled
      Time since boot: 30 days 23:29

$ system_profiler SPHardwareDataType
Hardware:

    Hardware Overview:

      Model Name: MacBook Pro
      Model Identifier: MacBookPro11,5
      Processor Name: Intel Core i7
      Processor Speed: 2.5 GHz
      Number of Processors: 1
      Total Number of Cores: 4
      L2 Cache (per Core): 256 KB
      L3 Cache: 6 MB
      Memory: 16 GB
      Boot ROM Version: MBP114.0183.B00
      SMC Version (system): 2.30f2
      Serial Number (system): XXXXXXXXXX
      Hardware UUID: XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXXX

```

### Pre Req : Anaconda 
Download : https://www.anaconda.com/download/#macos 

Python 3.6 version 64-Bit Distribution   

My anacoda installation  detail  : 

$ conda info

```
     active environment : None
            shell level : 0
       user config file : /Users/xx/.condarc
 populated config files : /Users/xx/.condarc
          conda version : 4.5.5
    conda-build version : 3.4.1
         python version : 3.6.4.final.0
       base environment : /anaconda3  (writable)
           channel URLs : https://repo.anaconda.com/pkgs/main/osx-64
                          https://repo.anaconda.com/pkgs/main/noarch
                          https://repo.anaconda.com/pkgs/free/osx-64
                          https://repo.anaconda.com/pkgs/free/noarch
                          https://repo.anaconda.com/pkgs/r/osx-64
                          https://repo.anaconda.com/pkgs/r/noarch
                          https://repo.anaconda.com/pkgs/pro/osx-64
                          https://repo.anaconda.com/pkgs/pro/noarch
          package cache : /anaconda3/pkgs
                          /Users/xx/.conda/pkgs
       envs directories : /anaconda3/envs
                          /Users/xx/.conda/envs
               platform : osx-64
             user-agent : conda/4.5.5 requests/2.18.4 CPython/3.6.4 Darwin/17.6.0 OSX/10.13.5
                UID:GID : 501:20
             netrc file : None
           offline mode : False
```



#### Step 1 : Create a virtual environment in conda  

$ conda create -n tensorflow pip python=3.6
```
Solving environment: done

## Package Plan ##

  environment location: /anaconda3/envs/tensorflow

  added / updated specs: 
    - pip
    - python=3.6


The following NEW packages will be INSTALLED:

    ca-certificates: 2018.03.07-0           
    certifi:         2018.4.16-py36_0       
    libcxx:          4.0.1-h579ed51_0       
    libcxxabi:       4.0.1-hebd6815_0       
    libedit:         3.1.20170329-hb402a30_2
    libffi:          3.2.1-h475c297_4       
    ncurses:         6.1-h0a44026_0         
    openssl:         1.0.2o-h26aff7b_0      
    pip:             10.0.1-py36_0          
    python:          3.6.6-hc167b69_0       
    readline:        7.0-hc1231fa_4         
    setuptools:      39.2.0-py36_0          
    sqlite:          3.24.0-ha441bb4_0      
    tk:              8.6.7-h35a86e2_3       
    wheel:           0.31.1-py36_0          
    xz:              5.2.4-h1de35cc_4       
    zlib:            1.2.11-hf3cbc9b_2 

Proceed ([y]/n)? y

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate tensorflow
#
# To deactivate an active environment, use
#
#     $ conda deactivate

```

#### Step 2 :  Activate environment 

$ conda activate tensorflow

#### Step 3 : Install tensorflow (As of version 1.2, TensorFlow no longer provides GPU support on macOS.)

(tensorflow)$ pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.8.0-py3-none-any.whl

```
Collecting tensorflow==1.8.0 from https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.8.0-py3-none-any.whl
  Downloading https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.8.0-py3-none-any.whl (46.5MB)
    100% |████████████████████████████████| 46.5MB 1.1MB/s 
Collecting protobuf>=3.4.0 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/6d/7e/51c91b28cb8446ebd7231d375a2025bca4c59d15ddc0cf2dd0867b400cd7/protobuf-3.6.0-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl (1.2MB)
    100% |████████████████████████████████| 1.2MB 7.7MB/s 
Collecting wheel>=0.26 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/81/30/e935244ca6165187ae8be876b6316ae201b71485538ffac1d718843025a9/wheel-0.31.1-py2.py3-none-any.whl (41kB)
    100% |████████████████████████████████| 51kB 17.2MB/s 
Collecting six>=1.10.0 (from tensorflow==1.8.0)
  Using cached https://files.pythonhosted.org/packages/67/4b/141a581104b1f6397bfa78ac9d43d8ad29a7ca43ea90a2d863fe3056e86a/six-1.11.0-py2.py3-none-any.whl
Collecting grpcio>=1.8.6 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/7e/a9/daef33ec8a83eb1c34498f947d4447d5728d91c7374e4b78465c7c14e99a/grpcio-1.13.0-cp36-cp36m-macosx_10_7_intel.whl (1.9MB)
    100% |████████████████████████████████| 1.9MB 10.7MB/s 
Collecting absl-py>=0.1.6 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/57/8d/6664518f9b6ced0aa41cf50b989740909261d4c212557400c48e5cda0804/absl-py-0.2.2.tar.gz (82kB)
    100% |████████████████████████████████| 92kB 18.9MB/s 
Collecting numpy>=1.13.3 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/f6/cd/b2c50b5190b66c711c23ef23c41d450297eb5a54d2033f8dcb3b8b13ac85/numpy-1.14.5-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl (4.7MB)
    100% |████████████████████████████████| 4.7MB 5.4MB/s 
Collecting gast>=0.2.0 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/5c/78/ff794fcae2ce8aa6323e789d1f8b3b7765f601e7702726f430e814822b96/gast-0.2.0.tar.gz
Collecting termcolor>=1.1.0 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/8a/48/a76be51647d0eb9f10e2a4511bf3ffb8cc1e6b14e9e4fab46173aa79f981/termcolor-1.1.0.tar.gz
Collecting astor>=0.6.0 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/35/6b/11530768cac581a12952a2aad00e1526b89d242d0b9f59534ef6e6a1752f/astor-0.7.1-py2.py3-none-any.whl
Collecting tensorboard<1.9.0,>=1.8.0 (from tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/59/a6/0ae6092b7542cfedba6b2a1c9b8dceaf278238c39484f3ba03b03f07803c/tensorboard-1.8.0-py3-none-any.whl (3.1MB)
    100% |████████████████████████████████| 3.1MB 9.2MB/s 
Collecting setuptools (from protobuf>=3.4.0->tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/7f/e1/820d941153923aac1d49d7fc37e17b6e73bfbd2904959fffbad77900cf92/setuptools-39.2.0-py2.py3-none-any.whl (567kB)
    100% |████████████████████████████████| 573kB 14.0MB/s 
Collecting markdown>=2.6.8 (from tensorboard<1.9.0,>=1.8.0->tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/6d/7d/488b90f470b96531a3f5788cf12a93332f543dbab13c423a5e7ce96a0493/Markdown-2.6.11-py2.py3-none-any.whl (78kB)
    100% |████████████████████████████████| 81kB 15.2MB/s 
Collecting bleach==1.5.0 (from tensorboard<1.9.0,>=1.8.0->tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/33/70/86c5fec937ea4964184d4d6c4f0b9551564f821e1c3575907639036d9b90/bleach-1.5.0-py2.py3-none-any.whl
Collecting werkzeug>=0.11.10 (from tensorboard<1.9.0,>=1.8.0->tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/20/c4/12e3e56473e52375aa29c4764e70d1b8f3efa6682bef8d0aae04fe335243/Werkzeug-0.14.1-py2.py3-none-any.whl (322kB)
    100% |████████████████████████████████| 327kB 9.7MB/s 
Collecting html5lib==0.9999999 (from tensorboard<1.9.0,>=1.8.0->tensorflow==1.8.0)
  Downloading https://files.pythonhosted.org/packages/ae/ae/bcb60402c60932b32dfaf19bb53870b29eda2cd17551ba5639219fb5ebf9/html5lib-0.9999999.tar.gz (889kB)
    100% |████████████████████████████████| 890kB 14.9MB/s 
Building wheels for collected packages: absl-py, gast, termcolor, html5lib
  Running setup.py bdist_wheel for absl-py ... done
  Stored in directory: /Users/aa/Library/Caches/pip/wheels/a0/f8/e9/1933dbb3447ea6ef57062fd5461cb118deb8c2ed074e8344bf
  Running setup.py bdist_wheel for gast ... done
  Stored in directory: /Users/aa/Library/Caches/pip/wheels/9a/1f/0e/3cde98113222b853e98fc0a8e9924480a3e25f1b4008cedb4f
  Running setup.py bdist_wheel for termcolor ... done
  Stored in directory: /Users/aa/Library/Caches/pip/wheels/7c/06/54/bc84598ba1daf8f970247f550b175aaaee85f68b4b0c5ab2c6
  Running setup.py bdist_wheel for html5lib ... done
  Stored in directory: /Users/aa/Library/Caches/pip/wheels/50/ae/f9/d2b189788efcf61d1ee0e36045476735c838898eef1cad6e29
Successfully built absl-py gast termcolor html5lib
Installing collected packages: six, setuptools, protobuf, wheel, grpcio, absl-py, numpy, gast, termcolor, astor, markdown, html5lib, bleach, werkzeug, tensorboard, tensorflow
Successfully installed absl-py-0.2.2 astor-0.7.1 bleach-1.5.0 gast-0.2.0 grpcio-1.13.0 html5lib-0.9999999 markdown-2.6.11 numpy-1.14.5 protobuf-3.6.0 setuptools-39.2.0 six-1.11.0 tensorboard-1.8.0 tensorflow-1.8.0 termcolor-1.1.0 werkzeug-0.14.1 wheel-0.31.1
```


#### Step 4 :Verify Installation 

Invoke python within the environment  and run following program 

```
import tensorflow as tf
hello = tf.constant('Hello, TensorFlow!')
sess = tf.Session()
print(sess.run(hello))
```
Expected Outcome :- 

    Hello, TensorFlow!

(tensorflow) $ python

```
Python 3.6.6 |Anaconda, Inc.| (default, Jun 28 2018, 11:07:29) 
[GCC 4.2.1 Compatible Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import tensorflow as tf
>>> hello = tf.constant('Hello, TensorFlow!')
>>> sess = tf.Session()
2018-07-06 17:06:13.742294: I tensorflow/core/platform/cpu_feature_guard.cc:140] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2 FMA
>>> print(sess.run(hello))
b'Hello, TensorFlow!'
```


Export environment

    conda env export > tensorflow.yml

Deactivate Environment

    source deactivate


create environmnet using yml file 

    conda env create -f tensorflow.yml
