!SLIDE bullets incremental transition=scrollRight
# Remote #
* It is where the distributed part comes in.
* git remot add &lt;alias&gt; &lt;URL&gt;
* You can add several remotes.

!SLIDE bullets incremental
# Pull #
* Fetch and merge changes in a remote.
* git pull &lt;repository&gt; &lt;refspec&gt;
* git pull &lt;remote&gt; &lt;branch&gt;

!SLIDE bullets incremental
# Push #
* Push the changes to another repo.
* _git push &lt;repository&gt; &lt;refspec&gt;_
* By default, pushes the branches in common with repository.
* _git push &lt;remote&gt; &lt;branch&gt;_

!SLIDE commandline incremental
    $ cd ..
    $ git clone new_repo new_remote
    $ cd new_repo
    $ git remote add my_remote file:///home/sergio/tmp/new_remote
    $ git pull my_remote master
    From file:///home/sergio/tmp/new_remote
     * branch            master     -> FETCH_HEAD
    Already up-to-date.
    $ echo "More info" >> README.txt
    $ git commit -a "More info"
    [master cee4433] More info
     1 files changed, 1 insertions(+), 0 deletions(-)
    $ cd ../new_remote

!SLIDE commandline incremental transition=scrollUp

    $ echo "ASNO (Another Stupid Number Ordering)" > asno
    $ git add asno
    $ git commit -m "asno"
    [master e4335b4] asno
     2 files changed, 1 insertions(+), 1 deletions(-)
     create mode 100644 asno
    $ cd ../new_repo
    $ git pull my_remote master 
    remote: Counting objects: 6, done.
    remote: Compressing objects: 100% (2/2), done.
    remote: Total 4 (delta 0), reused 1 (delta 0)
    Unpacking objects: 100% (4/4), done.
    From file:///home/sergio/tmp/new_remote
     * branch            master     -> FETCH_HEAD
    Updating cee4433..e4335b4
    Fast forward
     README.txt |    1 -
     asno       |    1 +
     2 files changed, 1 insertions(+), 1 deletions(-)
     create mode 100644 asno

!SLIDE bullets incremental
# Do not forget...#
* Only push if there is no other option.
* Be kind, ask for a pull request.
