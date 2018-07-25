# Pending

BREAKING CHANGES:
- [types] CanonicalTime uses nanoseconds instead of clipping to ms
    - breaks serialization/signing of all messages with a timestamp
- [abci] Removed Fee from ResponseDeliverTx and ResponseCheckTx
- [abci] Changed time format from int64 to google.protobuf.Timestamp

IMPROVEMENTS:
- [blockchain] Improve fast-sync logic
    - tweak params
    - only process one block at a time to avoid starving

BUG FIXES:
- [privval] fix a deadline for accepting new connections in socket private
  validator.
