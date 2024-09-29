rpi_tenserflowlite
==================

This role installs tenserflow lite on a Rasperry Pi.

As always: Use at your own risk!

Role Variables
--------------

| Name                      | Comment                                                         | Default value                |
|---------------------------|-----------------------------------------------------------------|------------------------------|
| tenserflowlite_user      | The user for which tenserflow lite will be installed            | pi |
| tenserflowlite_dir       | The target directory where tenserflow lite will be installed in | "/home/{{ tenserflow_lite_user }}/tensorflow/tensorflow_src" |
| tenserflowlite_version   | The version of tenserflow lite which will be installed          | `master` |
| tenserflowlite_model_url | The URL to the tenserflow model which will be used              | https://storage.googleapis.com/download.tensorflow.org/models/tflite/coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip |
| tenserflowlite_model_dir | The target directory got the downloaded tenserflow model        | "/home/{{ tenserflow_lite_user }}/tensorflow/model" |


Example Playbook
----------------
```yaml
- name: Raspberry Pi Tenserflow Lite
  hosts: tenserflow
  roles:
    - role: oxivanisher.raspberry_pi.rpi_tenserflowlite                     # install tenserflow lite
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.raspberry_pi](https://galaxy.ansible.com/ui/repo/published/oxivanisher/raspberry_pi/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-raspberry_pi).
