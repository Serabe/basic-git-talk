!SLIDE commandline incremental
# Stashing #

    $ echo "A brand new README file" > README.txt
    $ git status
    # On branch master
    # Changed but not updated:
    #	modified:   README.txt
    $ git stash
    Saved working directory and index state "WIP on master: e4335b4 asno"
    HEAD is now at e4335b4 asno
    (To restore them type "git stash apply")
    $ git stash list
    stash@{0}: WIP on master: e4335b4 asno

!SLIDE bullets incremental
# Stashing #

* Use stash to save changes without committing.
* Use stash list to show the _stashes_

!SLIDE commandline incremental
# Stashing #

    $ echo 'def hello;"hello";end;puts hello' > script.rb
    $ ruby script.rb
    hello
    $ git commit -a -m "Modified script."
    [master 7e42ebb] Modified script.
     1 files changed, 1 insertions(+), 1 deletions(-)
    $ cat README.txt 
    bye, bye beautiful
    $ git stash apply
    # On branch master
    # Changed but not updated:
    #
    #	modified:   README.txt
    $ cat README.txt 
    A brand new README file
    $ git commit -a -m "Brand new Readme"
    [master 74acb46] Brand new Readme
     1 files changed, 1 insertions(+), 1 deletions(-)
