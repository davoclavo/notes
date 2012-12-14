Etc notes
=========

### Spanish dict

From [this post](http://mx.answers.yahoo.com/question/index?qid=20090923123859AA0EO5m) downloaded [this file](ftp://ftp.gnu.org/gnu/aspell/dict/es/aspell6-es-1.11-2.tar.bz2)

then:

    tar xvjf aspell6-es-1.11-2.tar.tar.bz2 
    brew install aspell
    cd aspell6-es-1.11-2
    cat README
    ./configure
    make
    make install
    aspell -l es dump master | aspell -l es expand > lista.txt
    make clean


### Clean cache

    /Library/Caches/Homebrew/
