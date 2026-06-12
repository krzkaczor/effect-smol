---
"effect": patch
---

Fixed `Config.withDefault` silently falling back to the default value when a union/literal config (e.g. `Config.literals`, `Config.logLevel`) was given a present but invalid value (such as a misspelled literal). The default is now only applied when the value is genuinely missing; an invalid value fails as expected, closes #2384.
