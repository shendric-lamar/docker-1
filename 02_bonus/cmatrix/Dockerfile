FROM alpine

MAINTAINER shendric

RUN apk add --update --no-cache automake autoconf make ncurses-dev build-base git
RUN git clone https://github.com/abishekvashok/cmatrix.git

WORKDIR /cmatrix

RUN autoreconf -i
RUN ./configure
RUN make
RUN make install

CMD ["cmatrix"]

# docker build -t cmatrix .

# docker run --rm --log-driver none -it cmatrix
