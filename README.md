# Traefik Mesh

Traefik Mesh is a lightweight, non-invasive service mesh built on top of Traefik Proxy for Kubernetes. It provides automatic traffic management, observability, and security for microservices without requiring sidecar containers. Traefik Mesh is fully compliant with the Service Mesh Interface (SMI) specification and supports HTTP, TCP, and UDP traffic modes, traffic splitting, access control via TrafficTarget, rate limiting, circuit breaking, and retries.

**Website:** https://traefik.io/traefik-mesh  
**Documentation:** https://doc.traefik.io/traefik-mesh/  
**GitHub:** https://github.com/traefik/mesh

## APIs

### Traefik Mesh Controller API

The Traefik Mesh Controller API provides internal debugging and status endpoints for the Traefik Mesh controller pod. It exposes the current dynamic configuration built by the controller, the mesh topology, the readiness status of the controller, and per-node configuration for each Traefik Mesh proxy node.

- **Documentation:** https://doc.traefik.io/traefik-mesh/
- **OpenAPI:** [openapi/traefik-mesh-controller-openapi.yml](openapi/traefik-mesh-controller-openapi.yml)

## Artifacts

### OpenAPI Specs

| Spec | Description |
|------|-------------|
| [traefik-mesh-controller-openapi.yml](openapi/traefik-mesh-controller-openapi.yml) | Controller API for configuration, topology, and node status |

### Spectral Rules

| File | Description |
|------|-------------|
| [traefik-mesh-rules.yml](rules/traefik-mesh-rules.yml) | Spectral ruleset enforcing Traefik Mesh API conventions |

### Naftiko Capabilities

#### Shared Definitions

| File | Description |
|------|-------------|
| [shared/controller-api.yaml](capabilities/shared/controller-api.yaml) | Per-API consumed definition for the Controller API |

#### Workflow Capabilities

| File | Description |
|------|-------------|
| [mesh-operations.yaml](capabilities/mesh-operations.yaml) | Unified mesh operations — configuration, topology, node health (5 tools) |

### JSON Schemas

| File | Description |
|------|-------------|
| [traefik-mesh-pod-info-schema.json](json-schema/traefik-mesh-pod-info-schema.json) | Schema for mesh proxy node pod status |
| [traefik-mesh-service-entry-schema.json](json-schema/traefik-mesh-service-entry-schema.json) | Schema for Kubernetes service entries in the mesh |

### JSON Structure

| File | Description |
|------|-------------|
| [traefik-mesh-pod-info-structure.json](json-structure/traefik-mesh-pod-info-structure.json) | Structure documentation for PodInfo objects |

### JSON-LD

| File | Description |
|------|-------------|
| [traefik-mesh-context.jsonld](json-ld/traefik-mesh-context.jsonld) | JSON-LD context for Traefik Mesh linked data semantics |

### Examples

| File | Description |
|------|-------------|
| [traefik-mesh-get-nodes-example.json](examples/traefik-mesh-get-nodes-example.json) | Example response for GET /api/status/nodes |
| [traefik-mesh-get-configuration-example.json](examples/traefik-mesh-get-configuration-example.json) | Example response for GET /api/configuration/current |

### Vocabulary

| File | Description |
|------|-------------|
| [traefik-mesh-vocabulary.yml](vocabulary/traefik-mesh-vocabulary.yml) | Domain vocabulary for Traefik Mesh concepts |

## Maintainers

- **Kin Lane** (kin@apievangelist.com)
