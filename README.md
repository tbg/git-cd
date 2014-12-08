git-cd
======

easily `cd` to local git repositories.

Instead of

```bash
$ cd ~/Code/Go/src/github.com/cockroachdb/cockroach
...
$ cd ~/dotfiles
...
$ cd ~/Code/tschottdorf.github.io
...
$ cd ~/Code/Go/src/github.com/jpetazzo/docker-busybox
```

just type

```bash
$ gitcd cockroach
...
$ gitcd dotfiles
...
$ gitcd tscho*
...
$ gitcd *busybox
```

anywhere you are - just feed something unique to `gitcd` or it will simply give you the first thing it finds (try `gcd *` for a "surprise" git repository).

If you have repos with non-unique names (say I have `~/path1/cockroachdb/cockroach` and `~/path2/cockroach`) simply add a unique prefix:

```bash
$ gitcd cockroachdb/cockroach
~/path1/cockroachdb/cockroach
$ gitcd db/cockroach
~/path1/cockroachdb/cockroach
$ gitcd 2/cockroach
~/path2/cockroach
$ gitcd 2/co*ach
~/path2/cockroach
```

I'm assuming all your git repos are inside of your home directory. It's easy to adapt the script to pull the base directory from the env - feel free to PR this if you do need this.
