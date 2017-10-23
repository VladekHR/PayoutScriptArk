# Roadmap

Right now the functionalities of the payout script are limited. In the config
file I have already specified some functions that I want added to better serve
and help other delegates.

Here is a todo list for people willing to contribute:

1. `BLACKLIST` integration. This needs to be performed at the calculation level
   when parsing the blockchain.
2. Extending how `BALANCE_BRACKETS` should work. Currently `TMESTAMP_BRACKETS`
   allow you to set a higher share for early voters, depending on timestamps.
   `BALANCE_BRACKETS` should allow you to do the same based on a users balance:
   E.G. 200k Ark > 80% share, 100k Ark 90% Share, 50K Ark 96% Share
3. `MAX` and `MIN` balance need to be integrated at the calculation level to
   exclude certain voters (`MIN_BALANCE'), and allow voters to only vote with a
   maximal amount of Ark.
4. `COVER_VOTING_FEES`: I will probably add this myself, but basically a
   delegate should be able to allocate a certain amount of Ark each week to
   automatically cover someones voting fee. Restrictions need to be applied (so
   only once per account for example), as well as people removing their Ark
   balance shortly after should have 1 ark removed from their next payout and
   allocate that to their delegate.
5. Write a comprehensive guide for complete tech illiterates on how to create a
   node with a read-only role in the Ark-DB and setup the script using bash
6. Optional: write C++/C functions for parsing the blockchain to increase
   speeds.  (Not necessary at all at the moment, and it must be first confirmed
   that this would help. If the time spent is only in the database and network
   then this effect would be minimal at best.)