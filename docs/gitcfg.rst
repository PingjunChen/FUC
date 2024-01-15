git config
========

Git configuration
--------

User name

:code:`$ git config --global user.name PingjunChen`

User email

:code:`$ git config --global user.email pingjunchen@ieee.org`

Editor

:code:`$ git config --global core.editor vim`

Password

:code:`$ git config --global credential.helper store`

Default branch

:code:`$ git config --global init.defaultBranch main`

Add remote

:code:`$ git remote add origin https://github.com/user/repo.git`

Git alias
--------

.. code-block:: bash

    git config --global alias.cm "commit -m"
    git config --global alias.br branch
    git config --global alias.co checkout
    git config --global alias.cb "checkout -b"
    git config --global alias.last "log -1 HEAD"