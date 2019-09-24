Changelog
=========



продолжение следует


python3.7 -mvirtualenv --no-site-packages --no-download /home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest
/home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/python -m pip install --upgrade --cache-dir /home/docs/checkouts/readthedocs.org/user_builds/edi-n/.cache/pip pip
/home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/python -m pip install --upgrade --cache-dir /home/docs/checkouts/readthedocs.org/user_builds/edi-n/.cache/pip Pygments==2.3.1 setuptools==41.0.1 docutils==0.14 mock==1.0.1 pillow==5.4.1 alabaster>=0.7,<0.8,!=0.7.5 commonmark==0.8.1 recommonmark==0.5.0 sphinx<2 sphinx-rtd-theme<0.5 readthedocs-sphinx-ext<1.1
/home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/python -m pip install --exists-action=w --cache-dir /home/docs/checkouts/readthedocs.org/user_builds/edi-n/.cache/pip -r docs/requirements.txt
cat docs/conf.py
python /home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/sphinx-build -T -E -b readthedocs -d _build/doctrees-readthedocs -D language=ru . _build/html
python /home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/sphinx-build -T -b readthedocssinglehtmllocalmedia -d _build/doctrees-readthedocssinglehtmllocalmedia -D language=ru . _build/localmedia
python /home/docs/checkouts/readthedocs.org/user_builds/edi-n/envs/latest/bin/sphinx-build -b latex -D language=ru -d _build/doctrees . _build/latex
cat latexmkrc 

I've been just working on with something similar and I found the solution here. What you need to do is to use a custom directive and add it to an existing writer. You can simply add the directive (with small modifications) from the link to the rst2html.py script and you are all set. See 


.. container:: test
    :name: abrakadabra

    супер текст на который идет ссылка.... или нет
