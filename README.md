# music-cluster

a cli utility for dealing with local music collections


### setup (dev)

1. [install "virtualenvwrapper"](http://virtualenvwrapper.readthedocs.org/en/latest/install.html#basic-installation)
2. create virtualenv for python2.7 (because mutagen can't really parse tags on python3): `mkvirtualenv --python=/usr/bin/python2.7 music-cluster`
3. `pip install -r requirements.txt`
4. `workon music-cluster`


### testing

```bash
py.test

```


### usage

``` bash
python list.py [-h] [-t] [-p] [-d DEPTH] path

positional arguments:
  path                  path to list in

optional arguments:
  -h, --help            show this help message and exit
  -t, --tags            whether to print tags
  -p, --plain           plain text mode, effects disabled (colors, bold)
  -d DEPTH, --depth DEPTH
                        restricts level of subfolders

```
e.g. `python list.py ~/Music/ -t` prints something like:
![screenshot](https://raw.githubusercontent.com/markhovskiy/markhovskiy.github.io/master/uploads/music_cluster_screenshot.png)


### features/todo

- [x] print tree view of a folder (restrict depth, order subfiles by name)
- [x] use colors for file types
- [x] print tags table
- [ ] add functionality for checking a file tree against tags (e.g. `"<artist>" -> "<year> - <album>" -> "<track number> - <title>.mp3"`)
- [ ] introduce file-based configs for patterns, colors etc.
- [ ] add renaming capabilities (by patterns)
- [ ] add search capabilities
- [ ] take advantage of last.fm stats (e.g. http://www.last.fm/api/show/track.getTags)


### links

* http://mutagen.readthedocs.org/en/latest/api/id3.html
