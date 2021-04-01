Minimal reproduction repo for https://github.com/renovatebot/renovate/issues/9351

The bug is that renovate[bot] will immediately consider a branch committed to
by an other ignored bot as "stale" and rebase it, which under normal operation
will result in a bot war. For testing here, rather than triggering the other
bot on `pull_request`, I'm instead triggering it on any comment to
[issue #1](https://github.com/anomiex/renovate-test-2/issues/1). Comment on
that issue to trigger the bot if further testing is needed.
