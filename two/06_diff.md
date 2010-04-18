!SLIDE bullets incremental
# Diff #

* By default, shows changes between working tree and index.
* --numstat, --stat, --shortstat

!SLIDE commandline incremental

# More cowbell #

    $ echo 'def hello;"hello, world";end;puts hello' > script.rb
    $ ruby script.rb
    hello, world
    $ git add script.rb
    $ git commit -m "Added script"
    [master f78d882] Added script
     1 files changed, 1 insertions(+), 0 deletions(-)
    create mode 100644 script.rb

!SLIDE commandline incremental

# Diff #

    $ git diff --numstat f90b..f78d
    1       1       README.txt
    1       0       script.rb

    $ git diff --stat f90b..f78d
    README.txt |    2 +-
    script.rb  |    1 +
    2 files changed, 2 insertions(+), 1 deletions(-)

    $ git diff --shortstat f90b..f78d
    2 files changed, 2 insertions(+), 1 deletions(-)

!SLIDE commandline incremental
# Where did f90b..f78d come from? #

    $ git log --pretty=oneline
    f78d882af69ac823fe94411e97a8de91162a9380 Added script
    e1b7b899d2b5f672c3139aabc67b6a0e8a4032dc I need another commit
    f90b86beb4b99e88bf02ba3f6a7377d84617cf57 Initial commit

