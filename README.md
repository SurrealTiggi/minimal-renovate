# minimal-renovate

This is a repo to test renovate with a minimal config

## Current behavior

We've setup a template string in the `packageRules[].commitMessageTopic` field to use a handlebars template helper to dynamically write the PR title to include a path. The template helper however seems to not work at all, and instead outputs an empty string.

We can also see `{{baseDir}}` working since the branch in the PR uses it successfully
<img src="SCR-20230302-id0.png">

## Expected behavior

PR is opened with the following title:

_Update [production] flux release fluxcd/flux2 to v0.40.2_
