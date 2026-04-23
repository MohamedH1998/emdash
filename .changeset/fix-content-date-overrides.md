---
"emdash": patch
---

Fixes the REST content API silently stripping `publishedAt` on create/update and `createdAt` on create. Importers can now preserve original publish and creation dates on migrated content. Gated behind `content:publish_any` (EDITOR+) so regular contributors cannot backdate posts. `createdAt` is intentionally not accepted on update — `created_at` is treated as immutable.
