---
acl_categories:
- '@slow'
- '@transaction'
arity: 1
command_flags:
- noscript
- loading
- stale
- skip_slowlog
complexity: Depends on commands in the transaction
description: Executes all commands in a transaction.
group: transactions
hidden: false
linkTitle: EXEC
since: 1.2.0
summary: Executes all commands in a transaction.
syntax_fmt: EXEC
syntax_str: ''
title: EXEC
---
Executes all previously queued commands in a [transaction][tt] and restores the
connection state to normal.

[tt]: /topics/transactions

When using [`WATCH`](/commands/watch), `EXEC` will execute commands only if the watched keys were
not modified, allowing for a [check-and-set mechanism][ttc].

[ttc]: /topics/transactions#cas