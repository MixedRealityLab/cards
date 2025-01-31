# cards

Cards for Responsibility Jekyll website.

Peter Craigon & Chris Greenhalgh, University of Nottingham, 2024-2025

## Build

Basic Jekyll bootstrap...
```
sudo docker pull jekyll/jekyll
sudo docker run --rm -it --volume="$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll /bin/bash
```
```
chown -R jekyll /usr/gem/
bundle install
gem install webrick
```

Create (one time):
```
jekyll new docs
```

Build:
```
cd docs
jekyll build
```

Serve/test ()[http://localhost:4000]:
```
cd docs
sudo docker run --rm -it --name my-apache-app -p 8080:80 -v "$PWD"/_site:/usr/local/apache2/htdocs/cards/ httpd:2.4
```
or (not working):
```
jekyll serve
```