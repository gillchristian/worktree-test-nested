# worktree-test-nested

The companion repository for `worktree-test`. It is checked out *inside* the
parent at `notes/`, hidden from the parent by `.git/info/exclude`.

Its trunk is `main` while the parent's is `master` — deliberately, so that every
containment question about a mirror is proven to be asked against ITS trunk and
not the parent's.

`nested=(notes:mirror:fold)` means: every parent worktree gets a `notes/`
worktree on a branch of the same name, and once the parent's PR is merged, `wtx
rm` squash-merges that branch into `main` here, pushes, and deletes it.
