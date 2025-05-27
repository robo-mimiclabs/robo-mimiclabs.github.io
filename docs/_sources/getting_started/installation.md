# Welcome to MimicLabs!

You can use this repository to:
1. build your own tasks for a robot learning study
2. collect expert human teleoperated demonstrations
3. expand your datasets using MimicGen

# Installation

### 1. Setting up your conda environment
```bash
$ conda create -n mimiclabs python=3.10
$ conda activate mimiclabs
```

### 2. Installing supporting libraries
Run the following commands to install **Robosuite**, **LIBERO**, **MimicGen**, and **RoboCasa**.
```bash
# install LIBERO
(mimiclabs)$ git clone https://github.com/Lifelong-Robot-Learning/LIBERO.git
(mimiclabs)$ cd LIBERO
(mimiclabs)$ pip install -e .
(mimiclabs)$ cd ..

# install MimicGen
(mimiclabs)$ git clone https://github.com/NVlabs/mimicgen.git
(mimiclabs)$ cd mimicgen
(mimiclabs)$ pip install -e .
(mimiclabs)$ cd ..

# (optional) install RoboCasa (for additional assets)
(mimiclabs)$ git clone https://github.com/robocasa/robocasa.git
(mimiclabs)$ cd robocasa
(mimiclabs)$ pip install -e .
# next: follow instructions on their github to download robocasa assets

# install Robosuite
(mimiclabs)$ git clone https://github.com/ARISE-Initiative/robosuite.git
(mimiclabs)$ cd robosuite && git checkout b9d8d3de5e3dfd1724f4a0e6555246c460407daa
(mimiclabs)$ pip install -e .
(mimiclabs)$ cd ..
```

### 3. Installing MimicLabs
```bash
(mimiclabs)$ git clone <link_to_this_repo>
(mimiclabs)$ cd mimiclabs
(mimiclabs)$ pip install -e .
(mimiclabs)$ pip install -r requirements.txt
```

### 4. Downloading MimicLabs assets
```bash
(mimiclabs)$ cd mimiclabs/mimiclabs
(mimiclabs)$ python scripts/download_mimiclabs_assets.py
```
