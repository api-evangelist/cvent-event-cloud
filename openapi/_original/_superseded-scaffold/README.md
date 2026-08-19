# Superseded scaffold specs

These OpenAPI files were hand-written from Cvent's developer documentation ('best-effort spec
derived from Cvent developer portal documentation') by an earlier profiling pass, not harvested
from Cvent. They were superseded on 2026-08-13 when Cvent's own published OpenAPI specification
was located at https://github.com/cvent/rest-sdks/blob/main/cvent-public-spec/openapi.yaml — the
source of truth for Cvent's official TypeScript/.NET/Java SDKs.

They are retained here for provenance only. Do NOT derive artifacts from them: their paths are
wrong (they used /ea/webhooks where Cvent actually serves /hooks under the /ea base path) and
their operationIds were invented.
