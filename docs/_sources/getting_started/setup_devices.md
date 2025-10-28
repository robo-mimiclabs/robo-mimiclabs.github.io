# Setting up Data Collection Devices

We support data collection using a Meta Quest and a SpaceMouse in MimicLabs. Please follow instructions below to setup your device!

## Setting up Meta Quest as a teleop device

1. Clone and install `oculus_reader` repository in your conda environment.
```bash
$ git clone https://github.com/rail-berkeley/oculus_reader.git
$ cd oculus_reader
$ pip install -r requirements.txt
$ pip install -e .
```

2. Connect your Meta Quest using a USB-C cable and allow `USB Debugging`. For this step, you will need to put on your headset to allow reading from USB by clicking on a notification, and also confirm the boundary so the headset can stay in an immersive mode.

3. Setup adb.
```bash
# on MacOS
$ brew install android-platform-tools
$ adb devices
# make sure connected device is NOT listed as unauthorized
```

4. Install oculus_reader APK on the Meta Quest.
```bash
$ cd oculus_reader
$ python install.py
```

5. Test your installation.
```bash
$ python reader.py
```

## Setting up SpaceMouse as a teleop device

Setting up your SpaceMouse just requires installing `hidapi` in your python environment.

```bash
$ pip install hidapi
```

Simply connect the SpaceMouse using a USB cable and follow instructions for collecting demonstrations in MimicLabs.
