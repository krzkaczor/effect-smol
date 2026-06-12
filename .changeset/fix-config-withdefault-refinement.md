---
"effect": patch
---

Fixed `Config.withDefault` silently falling back to the default value when a refinement (a `Schema.check`/filter) rejected a present value. A refinement only runs on a value that has already decoded successfully, so a refinement failure is never missing data and now correctly fails instead of using the default.
