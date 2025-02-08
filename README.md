rpi_tensorflowlite
==================

This role installs tensorflow lite on a Rasperry Pi.

As always: Use at your own risk!

Role Variables
--------------

| Name                         | Comment                                                         | Default value                |
|------------------------------|-----------------------------------------------------------------|------------------------------|
| rpi_tensorflowlite_user      | The user for which tensorflow lite will be installed            | pi |
| rpi_tensorflowlite_dir       | The target directory where tensorflow lite will be installed in | "/home/{{ tensorflow_lite_user }}/tensorflow/tensorflow_src" |
| rpi_tensorflowlite_version   | The version of tensorflow lite which will be installed          | `master` |
| rpi_tensorflowlite_model_url | The URL to the tensorflow model which will be used              | https://storage.googleapis.com/download.tensorflow.org/models/tflite/coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip |
| rpi_tensorflowlite_model_dir | The target directory got the downloaded tensorflow model        | "/home/{{ tensorflow_lite_user }}/tensorflow/model" |


Example Playbook
----------------
```yaml
- name: Raspberry Pi tensorflow Lite
  hosts: tensorflow
  roles:
    - role: oxivanisher.raspberry_pi.rpi_tensorflowlite
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.raspberry_pi](https://galaxy.ansible.com/ui/repo/published/oxivanisher/raspberry_pi/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-raspberry_pi).
