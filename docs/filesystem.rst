filesystem
========

Check specifc lines inside a text file
--------

:code:`$ sed -n <start_line_num>:<end_line_num>p <text_file>`

Find files contain specifc text
--------

:code:`$ grep -rin <text> .`

Storage usage
--------

Check disk partition usage

:code:`$ df -h`

Check the size of a directory

:code:`$ du -hs <directory>`

Check size of all subdirectories
--------

:code:`$ du -hs *`

Sync folder A into folder B
--------

.. code-block:: bash

    $ rsync -avu --delete folderA_path/ folderB_path
    Options:
        -a                                        # sync preserving all filesystem attributes
        -v                                        # run verbosely
        -u                                        # only copy files with a newer modification time 
        --delete                                  # delete the files in target folder that do not exist in the source
        folderA_path/                             # slash is required
        folderB_path                              # slash not required

Searches directory recursively in subdirectories
--------

:code:`$ find . -type d -name <directory>`

Searches file recursively in subdirectories
--------

:code:`$ find . -type f -name <file>`

Delete file/directory recursively in subdirectories
--------

:code:`$ find . -name <file/directory> -exec rm -rf {} \\;`

Get number of all files
--------
When number of file is small, less than 10, 000

:code:`$ ls -ls *.<ext> | wc -l`

When more than 10, 000 files

:code:`$ find -type f -name '*.<ext>'  | wc -l`

