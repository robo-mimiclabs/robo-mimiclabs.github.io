# Data collection in MimicLabs

We support data collection using a Meta Quest and a SpaceMouse in MimicLabs. Please follow instructions in `docs/installation/setup_devices.md` to setup your device before collecting expert demonstrations for the tasks your created.

## Collecting expert demonstrations

After having set up your task config, use our provided script to collect demonstrations for your task:
```bash
(myenv)$ cd <PATH_TO_MIMICLABS>/mimiclabs/data_collection/sim
(myenv)$ python scripts/collect_data.py \
    --task_suite_name <YOUR/TASK/SUITE> \
    --task_name <TASK_NAME> \
    --robots Panda \
    --control_delta \
    --device <DEVICE_NAME>
```
For an example, you can replace `<YOUR/TASK/SUITE>` with `test_suite` and `<TASK_NAME>` with `test_task`. This will spin-up data collection for the task config located at `mimiclabs/task_suites/test_siute/test_task.bddl` in this repo. Note that `<YOUR/TASK/SUITE>` can be a directory tree and does not necessarily have to be a single directory.

You can specify your choice of device by replacing `<DEVICE_NAME>` with `spacemouse` or `quest`.

By default, demos will be stored under `<PATH_TO_MIMICLABS>/mimiclabs/data_collection/sim/demos/<YOUR/TASK/SUITE>/<TASK_NAME>`.

Once collected, run the following script to post-process demos and save them into a single hdf5 file.
```bash
(myenv)$ python scripts/postprocess_demos.py --demo_dir <PATH/TO/COLLECTED/DEMOS>
```

To expand the collected source demonstrations, follow instructions in the next tutorial.

## Controls

### Meta Quest

- Left controller: move robot
- Right controller: move second robot (if applicable)
- A button: save demo at any stage (saving also automatically happens when task is done)
- B button: delete current demo, and start a new one
- ctrl+C: discard current demo and exit

### SpaceMouse

- Joystick: move robot
- Right button: start data collection / discard demo
- Left button: toggle gripper
- ctrl+C: discard current demo and exit

<!-- TODO add playback_demo.py; make a note that camera view in data collection is frontview but that in playback is the one reset by the bddl. -->