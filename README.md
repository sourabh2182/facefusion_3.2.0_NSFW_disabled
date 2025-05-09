FaceFusion
==========

> Industry leading face manipulation platform.

[![Build Status](https://img.shields.io/github/actions/workflow/status/facefusion/facefusion/ci.yml.svg?branch=master)](https://github.com/facefusion/facefusion/actions?query=workflow:ci)
[![Coverage Status](https://img.shields.io/coveralls/facefusion/facefusion.svg)](https://coveralls.io/r/facefusion/facefusion)
![License](https://img.shields.io/badge/license-OpenRAIL--AS-green)


Preview
-------

![Preview](https://raw.githubusercontent.com/facefusion/facefusion/master/.github/preview.png?sanitize=true)


Installation
------------

Be aware, the [installation](https://docs.facefusion.io/installation) needs technical skills and is not recommended for beginners. In case you are not comfortable using a terminal, our [Windows Installer](http://windows-installer.facefusion.io) and [macOS Installer](http://macos-installer.facefusion.io) get you started.


Usage
-----

Run the command:

```
python facefusion.py [commands] [options]

options:
  -h, --help                                      show this help message and exit
  -v, --version                                   show program's version number and exit

commands:
    run                                           run the program
    headless-run                                  run the program in headless mode
    batch-run                                     run the program in batch mode
    force-download                                force automate downloads and exit
    job-list                                      list jobs by status
    job-create                                    create a drafted job
    job-submit                                    submit a drafted job to become a queued job
    job-submit-all                                submit all drafted jobs to become a queued jobs
    job-delete                                    delete a drafted, queued, failed or completed job
    job-delete-all                                delete all drafted, queued, failed and completed jobs
    job-add-step                                  add a step to a drafted job
    job-remix-step                                remix a previous step from a drafted job
    job-insert-step                               insert a step to a drafted job
    job-remove-step                               remove a step from a drafted job
    job-run                                       run a queued job
    job-run-all                                   run all queued jobs
    job-retry                                     retry a failed job
    job-retry-all                                 retry all failed jobs
```


Documentation
-------------

# Face Fusion 3.2.0 NSFW disabled Installation





## 1. Prepare Your Platform for Windows






## Git

```bash
  winget install -e --id Git.Git
```

## Conda

```bash
  winget install -e --id Anaconda.Miniconda3 --override "/AddToPath=1"
```
    
## FFmpeg

```bash
winget install -e --id Gyan.FFmpeg
```

## 2. Prepare Your Environment
#### Initialize conda for your terminal:

```bash
conda init --all
```
#### Create the environment:

```bash
conda create --name facefusion python=3.12 pip=25.0
```
#### Activate the environment:

```bash
conda activate facefusion
```

## 3. Install Your Accelerator
## CUDA
#### Compatible with NVIDIA graphic cards:
```bash
 conda install conda-forge::cuda-runtime=12.8.1 conda-forge::cudnn=9.8.0.87
```
## TensorRT (Can be ommitted for windows)
#### Suitable for high performance NVIDIA graphic cards: 
```bash
 pip install tensorrt==10.9.0.34 --extra-index-url https://pypi.nvidia.com
```

)

## OpenVINO
#### Suitable for Intel Arc graphic cards: 
```bash
 conda install conda-forge::openvino=2025.1.0
```

## 4. Download Your Copy

#### Clone the repository:

```bash
git clone https://github.com/sourabh2182/facefusion_3.2.0_NSFW_disabled.git
```

#### Ensure to enter the directory:

```bash
cd facefusion
```

## 5. Install The Application
#### CPU:

```bash
python install.py --onnxruntime default
```
#### CUDA:

```bash
python install.py --onnxruntime cuda
```

## 6. Reload Your Environment
```bash
conda deactivate
```
```bash
conda activate facefusion
```

## 7. Done
#### Finally, run the program:

```bash
python facefusion.py run --open-browser
```
