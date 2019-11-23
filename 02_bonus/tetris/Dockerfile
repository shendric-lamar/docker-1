FROM ubuntu

MAINTAINER shendric

RUN apt-get update && apt-get install -y emacs

CMD ["/usr/bin/emacs", "-f", "tetris"]

# docker build -t tetris .

# docker run --rm -ti tetris
