JapScanDownloader
=================

|Codacy Badge| |Build Status| |License: GPL v3| |codecov|

Installation
------------

Auto
~~~~

pip install -r requirements.txt

Dependencies
~~~~~~~~~~~~

-  `Beautiful Soup 4`_
-  `PyYAML`_
-  `tqdm`_
-  `lxml`_
-  `Pillow`_
-  `cloudscraper`_

Usage
-----

Run
~~~

.. code:: bash

   python japscandownloader/main.py

Options
~~~~~~~

.. code:: bash

   usage: main.py [-h] [-c CONFIG_FILE] [-d DESTINATION_PATH] [-f FORMAT] [-v]
                  [-r] [-k] [-u]

   optional arguments:
     -h, --help            show this help message and exit
     -c CONFIG_FILE, --config_file CONFIG_FILE
                           Set config file Example : python
                           japscandownloader/main.py -c /home/myconfigfile.yml
     -d DESTINATION_PATH, --destination_path DESTINATION_PATH
                           Set destination path of downloaded mangas Example :
                           python japscandownloader/main.py -d /home/mymangas/
     -f FORMAT, --format FORMAT
                           Set format of downloaded mangas Example : python
                           japscandownloader/main.py -f cbz|pdf|jpg|png
     -v, --verbose         Active verbose mode, support different level Example :
                           python japscandownloader/main.py -vv
     -r, --reverse         Reverse chapters download order (Default : Last to
                           first) Example : python japscandownloader/main.py -r
     -k, --keep            Keep downloaded images (when format is pdf/cbz)
                           (default : false) Example : python
                           japscandownloader/main.py -k
     -u, --unscramble      Force unscrambling Example : python
                           japscandownloader/main.py -u

How it work
~~~~~~~~~~~

This program use an config file (default : ./config.yml)

This file contains list of mangas to download, destination path, etc.

Example of config file
^^^^^^^^^^^^^^^^^^^^^^

\``\` yaml mangas: - chapter:
https://www.japscan.to/lecture-en-ligne/shingeki-no-kyojin/60/

-  url: https://www.japscan.to/manga/uq-holder/

-  chapters: url: https://www.japscan.to/lecture-en-ligne/black-clover/
   chapter_min: 158 chapter_max: 197

destinatio

.. _Beautiful Soup 4: https://www.crummy.com/software/BeautifulSoup/bs4/doc/
.. _PyYAML: https://github.com/yml/pyyml
.. _tqdm: https://github.com/tqdm/tqdm
.. _lxml: https://github.com/lxml/lxml.git
.. _Pillow: https://github.com/python-pillow/Pillow.git
.. _cloudscraper: https://github.com/VeNoMouS/cloudscraper

.. |Codacy Badge| image:: https://api.codacy.com/project/badge/Grade/acf59998d8a743188d5f7ef058010ffa
   :target: https://www.codacy.com/app/Harkame/JapScanDownloader?utm_source=github.com&utm_medium=referral&utm_content=Harkame/JapScanDownloader&utm_campaign=Badge_Grade
.. |Build Status| image:: https://travis-ci.org/Harkame/JapScanDownloader.svg?branch=master
   :target: https://travis-ci.org/Harkame/JapScanDownloader
.. |License: GPL v3| image:: https://img.shields.io/badge/License-GPLv3-blue.svg
   :target: https://www.gnu.org/licenses/gpl-3.0
.. |codecov| image:: https://codecov.io/gh/Harkame/JapScanDownloader/branch/master/graph/badge.svg
   :target: https://codecov.io/gh/Harkame/JapScanDownloader
