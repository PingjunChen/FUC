seadragon
========

`Seadragon <http://hpcweb.mdanderson.org/>`_ is a  supercomputing resource of
MD Anderson’s High Performance Computing (HPC), which is dedicated for use by
the research community.

Login Seadragon
--------

.. code-block:: bash

    $ ssh seadragon


Interactive Running
--------

.. code-block:: bash

    # cpu interactive
    $ busb -Is -q interactive -W 1:00 -M 64 -R rusage[mem=64] –n 4 /bin/bash
    # gpu interactive
    $ busb -Is -q gpu-medium -gpu num=1:gmem=16 -W 3:00 -M 64 -R rusage[mem=64] –n 10 /bin/bash


Load Modules
--------

.. code-block:: bash

    $ module load kubectl
    $ module load singularity/3.5.2
    $ module load cuda10.1/toolkit/10.1.243


Start Singularity Instance
--------

.. code-block:: bash

    $ singularity run --nv --bind <local_dir>:<container_dir> <singularity_path> <program>


More Useful Commands
--------

.. code-block:: bash

    $ bsub < <lsf_script> # submit job via script
    $ bjobs -u all | more # check all running jobs
    $ bjobs -u all | grep gpu # check all gpu jobs
    $ bjobs -p # show all pending jobs
    $ bjobs -l xxxxxxx # check the details of one specific job
    $ bkill -l xxxxxxx # kill one specific job
