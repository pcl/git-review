# `git review`: format git diffs in a friendly manner

## Usage

```sh
# See an overview of the commits between HEAD and origin/master
$ git review --stat origin/master..

# See the diffs in each commit, each internally sorted and formatted
# according to the rules in the commit message
$ git review origin/master..
```

## Installation

```sh
curl https://raw.githubusercontent.com/pcl/git-review/master/src/git-review > git-review
mv git-review ~/bin/
chmod u+x ~/bin/git-review
```

## What does this do?

`git review` is roughly the equivalent to `git log -p`, taking into
account any `Review-Options` trailers specified in the commit
messages.

To see it in action, run `test/test-git-review` and notice that the
`important` file is listed before the others, in contrast to the
output of `git show`.
