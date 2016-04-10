lac.linuxaudio.org
##################
| This is the README for http://lac.linuxaudio.org
|
| The website is constructed from

* a |pelican| project (all content as reStructuredText, see *reStructuredText_CheatSheet.txt* for help).
* a subset of |pelican-plugins|, which are a submodule of this repository in the folder **pelican-plugins**
*i a customized theme - have a look at the **theme** folder

Getting the content
-------------------

* Clone the repository

  .. code:: bash

    git clone https://github.com/linuxaudio/lac.linuxaudio.org

* Initialize all submodules

  .. code:: bash

    git submodule update --init --recursive

Generating new content
----------------------
| After editing pages or blog posts, re-generate the whole site by doing a simple

  .. code:: bash

    pelican

| in the root directory of this repository. It will generate the whole website below the **output** folder.

Testing new content locally
---------------------------
| You can easily locally test your changes by starting a simple python HTTP server for the **output** folder.

  .. code:: bash

    cd output
    python -m http.server

| This will start the web server on your |localhost| on port 8000, so you can easily have a look at your modifications.
| (You can also use the **develop_server.sh** script in the root of this repository for this.)

Upload new content to the webserver
-----------------------------------
| Uploading the new content now is as easy as doing a 

  .. code:: bash

    make rsync_upload

| in the root directory of this repository.
| This will automatically rsync the output folder with your remote website folder.



.. |pelican| raw:: html

  <a href="https://getpelican.com" target="_blank">Pelican</a>

.. |pelican-plugins| raw:: html

  <a href="https://github.com/getpelican/pelican-plugins/" target="_blank">Pelican Plugins</a>

.. |localhost| raw:: html

  <a href="localhost:8000" target="_blank">localhost</a>

