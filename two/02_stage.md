!SLIDE bullets incremental transition=scrollDown
# Stage #

* What is it?
* Is it really necessary?
* Tell me more, tell me more (Was it love at first sight?)

!SLIDE commandline incremental
# Adding a file #
    $ touch README.txt
    $ echo hello, world > README.txt
    $ cat README.txt
    hello, world
    $ git add README.txt
    $ git status
    # Changes to be committed:
    #       new file:   README.txt

!SLIDE commandline incremental
# Removing a file #
    $ git rm --cached README.txt
    $ git status
    # Untracked files:
    #       README.txt
    $ ls
    README.txt
    $ git add README.txt

!SLIDE bullets incremental

# What's next? #
* Committing
* Log
* Diff
* Branching
