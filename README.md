# git-review: format git diffs in a friendly manner


Equivalent to `git show`, taking into account any `Review-Options`
trailers specified in the commit messages. For implementation
simplicity, this aggregates the trailers for all messages in the
commit-spec, rather than applying them on a per-commit basis.

To see it in action, run `test/test-git-review` and notice that the
`important` file is listed before the others, in contrast to the
output of `git show`.
