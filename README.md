
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

