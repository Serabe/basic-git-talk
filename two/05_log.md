!SLIDE commandline incremental
# A few more changes #

    $ echo bye, bye beautiful > README.txt
    $ cat README.txt
    bye, bye beautiful
    $ git commit -a -m "I need another commit"
    [mater e1b7b89] I need another commit
     1 files changed, 1 insertions(+), 1 deletions(-)

!SLIDE commandline incremental
# Log: example #
    $ git log
    commit e1b7b899d2b5f672c3139aabc67b6a0e8a4032dc
    Author: Sergio Arbeo <serabe@gmail.com>
    Date:   Sun Apr 18 17:22:09 2010 +0200

        I need another commit

    commit f90b86beb4b99e88bf02ba3f6a7377d84617cf57
    Author: Sergio Arbeo <serabe@gmail.com>
    Date:   Sun Apr 18 17:11:49 2010 +0200

        Initial commit

!SLIDE bullets incremental
# Log: info showed #
* SHA1
* Author
* Date
* Full commit message

!SLIDE bullets incremental
# Log: options #
* --pretty [oneline|short|medium|full|fuller|email|raw]
* -n N: number of commits to show.
* --since="1 year ago"
* --until=today

!SLIDE commandline incremental
# Log example #
    $ git log -n 7 --oneline --since="2 days ago"
    940ef1a Do not go through RubyString in Kernel#...
    245fe4e In 1.9, Kernel#global_variables, Kernel#...
    a531f14 Fix jruby.jit.maxsize help text.
    8c9d4ce Use gemcutter when releasing, and...
    61c620a Fix JRUBY-4715 FFI::StructByValue...
