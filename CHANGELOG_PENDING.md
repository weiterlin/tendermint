# Pending

BREAKING CHANGES:
- [types] CanonicalTime uses nanoseconds instead of clipping to ms
    - breaks serialization/signing of all messages with a timestamp
- [abci] Removed Fee from ResponseDeliverTx and ResponseCheckTx
- [p2p] Remove salsa and ripemd primitives, in favor of using chacha as a stream cipher, and hkdf

IMPROVEMENTS:
- [blockchain] Improve fast-sync logic
    - tweak params
    - only process one block at a time to avoid starving

BUG FIXES:
- [privval] fix a deadline for accepting new connections in socket private
  validator.
