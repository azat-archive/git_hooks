
Custom hooks for GIT.
=====================

Remote
------

- `update-beauty`

    patches/commits beauty (linux only, because of some options for grep)  
    Test commit separatly, and can check newly created refs
- `update-beauty-one-pass`

    The same as previous, but test commits together  
    And because of this can't test newly created refs.
- `pre-receive-beauty`

    The same as `update-beauty`, but at `pre-receive` state.

- `post-receive-email`

    Custom version of original post-receive-email hook (see https://github.com/git/git/blob/master/contrib/hooks/post-receive-email)
    Plus new options and features:

        - hooks.scancommitforcc
            If this option is set to true, than commit messages will be scanned for
            "Cc:" line and parse it for emails, and add this emails to recipients list
            Default: false

        - hooks.scancommitforemails
            If this option is set to true, than commit messages will be scanned for
            all emails, and add this emails to recipients list
            Default: false

    For more info see here https://github.com/azat/git/compare/git:master...hooks.scancommitforcc
