FROM debian

MAINTAINER shendric

RUN apt-get update && apt-get install -y cowsay fortune lolcat

ENTRYPOINT /usr/games/fortune | /usr/games/cowsay | /usr/games/lolcat

# add echo "text" to customize quote.

# add -f dragon or -f ren for fun.

# docker build -t cowsay .

# docker run --rm -ti cowsay
