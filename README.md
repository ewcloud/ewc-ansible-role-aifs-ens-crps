EWC Ansible Role AIFS ENS CRPS
================================

Create a conda environment with AIFS ENS CRPS and associated software stack.

Requirements
------------

This ansible role depends on ewc-ansible-role-conda and needs to be applied on a GPU-powered instance.

Role Variables
--------------

- `aifs_ens_crps_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: no
- `aifs_ens_crps_env_name`: Name of the environment containing the software stack. Default: aifs-ens-crps
- `aifs_ens_crps_env_path`: Installation path for the environment. Default: "{{ conda_prefix }}/envs/{{ aifs_ens_crps_env_name }}"
- `aifs_ens_crps_checkpoint`: URL to the model checkpoint. Default: [https://huggingface.co/ecmwf/aifs-ens-1.0/resolve/main/aifs-ens-crps-1.0.ckpt](https://huggingface.co/ecmwf/aifs-ens-1.0/resolve/main/aifs-ens-crps-1.0.ckpt)
- `aifs_ens_crps_create_ipykernel`: Create the jupyter kernel for this environment. Default: yes
- `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
- `conda_user`: User owning the conda installation. Default: `root`

Example Playbook
----------------

    - hosts: all
      roles:
         -  ewc-ansible-role-aifs-ens-crps

License
-------

Apache 2.0.

Author Information
------------------

ECMWF for the European Weather Cloud
