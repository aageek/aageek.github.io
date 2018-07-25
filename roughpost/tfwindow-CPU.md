$ conda env list
$ conda create -n tensorflow pip python=3.6
```
Solving environment: done


==> WARNING: A newer version of conda exists. <==
  current version: 4.4.10
  latest version: 4.5.8

Please update conda by running

    $ conda update -n base conda



## Package Plan ##

  environment location: C:\anaconda3\envs\tensorflow

  added / updated specs:
    - pip
    - python=3.6


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    wincertstore-0.2           |           py36_1          13 KB  conda-forge
    setuptools-40.0.0          |           py36_0         568 KB  conda-forge
    python-3.6.5               |                1        19.5 MB  conda-forge
    vs2015_runtime-14.0.25420  |                0         1.9 MB  conda-forge
    wheel-0.31.1               |           py36_0          79 KB  conda-forge
    pip-9.0.3                  |           py36_0         1.8 MB  conda-forge
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
wincertstore 0.2: ########################################################################################################################################################################################################################################## | 100%
setuptools 40.0.0: ######################################################################################################################################################################################################################################### | 100%
python 3.6.5: ############################################################################################################################################################################################################################################## | 100%
vs2015_runtime 14.0.25420: ################################################################################################################################################################################################################################# | 100%
wheel 0.31.1: ############################################################################################################################################################################################################################################## | 100%
pip 9.0.3: ################################################################################################################################################################################################################################################# | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use:
# > activate tensorflow
#
# To deactivate an active environment, use:
# > deactivate
#
# * for power-users using bash, you must source
#
```

$ source activate tensorflow
(tensorflow) $ pip install --ignore-installed --upgrade tensorflow
```
Collecting tensorflow
  Downloading https://files.pythonhosted.org/packages/e7/88/417f18ca7eed5ba9bebd51650d04a4af929f96c10a10fbb3302196f8d098/tensorflow-1.9.0-cp36-cp36m-win_amd64.whl (37.1MB)
    100% |████████████████████████████████| 37.1MB 31kB/s
Collecting gast>=0.2.0 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/5c/78/ff794fcae2ce8aa6323e789d1f8b3b7765f601e7702726f430e814822b96/gast-0.2.0.tar.gz
Collecting grpcio>=1.8.6 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/d5/c6/15728549704f9c03db7179b7f99303b91b7703e18a50f5e7b47e59b289ea/grpcio-1.13.0-cp36-cp36m-win_amd64.whl (1.4MB)
    100% |████████████████████████████████| 1.4MB 608kB/s
Collecting termcolor>=1.1.0 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/8a/48/a76be51647d0eb9f10e2a4511bf3ffb8cc1e6b14e9e4fab46173aa79f981/termcolor-1.1.0.tar.gz
Collecting absl-py>=0.1.6 (from tensorflow)
  Cache entry deserialization failed, entry ignored
  Downloading https://files.pythonhosted.org/packages/57/8d/6664518f9b6ced0aa41cf50b989740909261d4c212557400c48e5cda0804/absl-py-0.2.2.tar.gz (82kB)
    100% |████████████████████████████████| 92kB 3.1MB/s
Collecting astor>=0.6.0 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/35/6b/11530768cac581a12952a2aad00e1526b89d242d0b9f59534ef6e6a1752f/astor-0.7.1-py2.py3-none-any.whl
Collecting protobuf>=3.4.0 (from tensorflow)
  Cache entry deserialization failed, entry ignored
  Downloading https://files.pythonhosted.org/packages/75/7a/0dba607e50b97f6a89fa3f96e23bf56922fa59d748238b30507bfe361bbc/protobuf-3.6.0-cp36-cp36m-win_amd64.whl (1.1MB)
    100% |████████████████████████████████| 1.1MB 775kB/s
Collecting tensorboard<1.10.0,>=1.9.0 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/9e/1f/3da43860db614e294a034e42d4be5c8f7f0d2c75dc1c428c541116d8cdab/tensorboard-1.9.0-py3-none-any.whl (3.3MB)
    100% |████████████████████████████████| 3.3MB 290kB/s
Collecting setuptools<=39.1.0 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/8c/10/79282747f9169f21c053c562a0baa21815a8c7879be97abd930dbcf862e8/setuptools-39.1.0-py2.py3-none-any.whl (566kB)
    100% |████████████████████████████████| 573kB 1.3MB/s
Collecting six>=1.10.0 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/67/4b/141a581104b1f6397bfa78ac9d43d8ad29a7ca43ea90a2d863fe3056e86a/six-1.11.0-py2.py3-none-any.whl
Collecting numpy>=1.13.3 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/0d/b7/0c804e0bcba6505f8392d042d5e333a5e06f308e019517111fbc7767a0bc/numpy-1.14.5-cp36-none-win_amd64.whl (13.4MB)
    100% |████████████████████████████████| 13.4MB 91kB/s
Collecting wheel>=0.26 (from tensorflow)
  Downloading https://files.pythonhosted.org/packages/81/30/e935244ca6165187ae8be876b6316ae201b71485538ffac1d718843025a9/wheel-0.31.1-py2.py3-none-any.whl (41kB)
    100% |████████████████████████████████| 51kB 2.1MB/s
Collecting markdown>=2.6.8 (from tensorboard<1.10.0,>=1.9.0->tensorflow)
  Cache entry deserialization failed, entry ignored
  Downloading https://files.pythonhosted.org/packages/6d/7d/488b90f470b96531a3f5788cf12a93332f543dbab13c423a5e7ce96a0493/Markdown-2.6.11-py2.py3-none-any.whl (78kB)
    100% |████████████████████████████████| 81kB 2.7MB/s
Collecting werkzeug>=0.11.10 (from tensorboard<1.10.0,>=1.9.0->tensorflow)
  Downloading https://files.pythonhosted.org/packages/20/c4/12e3e56473e52375aa29c4764e70d1b8f3efa6682bef8d0aae04fe335243/Werkzeug-0.14.1-py2.py3-none-any.whl (322kB)
    100% |████████████████████████████████| 327kB 1.4MB/s
Building wheels for collected packages: gast, termcolor, absl-py
  Running setup.py bdist_wheel for gast ... done
  Stored in directory: C:\Users\abhanand\AppData\Local\pip\Cache\wheels\9a\1f\0e\3cde98113222b853e98fc0a8e9924480a3e25f1b4008cedb4f
  Running setup.py bdist_wheel for termcolor ... done
  Stored in directory: C:\Users\abhanand\AppData\Local\pip\Cache\wheels\7c\06\54\bc84598ba1daf8f970247f550b175aaaee85f68b4b0c5ab2c6
  Running setup.py bdist_wheel for absl-py ... done
  Stored in directory: C:\Users\abhanand\AppData\Local\pip\Cache\wheels\a0\f8\e9\1933dbb3447ea6ef57062fd5461cb118deb8c2ed074e8344bf
Successfully built gast termcolor absl-py
Installing collected packages: gast, six, grpcio, termcolor, absl-py, astor, setuptools, protobuf, markdown, numpy, wheel, werkzeug, tensorboard, tensorflow
Successfully installed absl-py-0.2.2 astor-0.7.1 gast-0.2.0 grpcio-1.13.0 markdown-2.6.11 numpy-1.14.5 protobuf-3.6.0 setuptools-40.0.0 six-1.11.0 tensorboard-1.9.0 tensorflow-1.9.0 termcolor-1.1.0 werkzeug-0.14.1 wheel-0.31.1
Cache entry deserialization failed, entry ignored
You are using pip version 9.0.3, however version 10.0.1 is available.
You should consider upgrading via the 'python -m pip install --upgrade pip' command.
```

$python
```
>>> import tensorflow as tf
>>> hello = tf.constant('Hello, TensorFlow!')
>>> sess = tf.Session()
2018-07-12 17:20:00.101940: I T:\src\github\tensorflow\tensorflow\core\platform\cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2
>>> print(sess.run(hello))
b'Hello, TensorFlow!'
```


$ conda env list
```
# conda environments:
#
                         C:\Users\abhanand\.julia\v0.6\Conda\deps\usr
base                     C:\anaconda3
tensorflow            *  C:\anaconda3\envs\tensorflow
```