# RKD-01: Build on praecepta DDD/ES Framework

**Status:** Accepted
**Source:** VISION.md D1

## Decision

Build redkiln on the praecepta DDD/ES framework rather than raw eventsourcing library.

## Rationale

Consistent patterns (BaseAggregate, BaseEvent, BaseProjection), multi-tenancy built-in, import-linter boundary enforcement, auto-discovery via entry points.

## Alternatives Considered

Raw eventsourcing + custom patterns.

## See Also

- See `pyproject.toml` for praecepta dependency declarations
