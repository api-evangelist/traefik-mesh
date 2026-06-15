# Traefik Mesh (traefik-mesh)

Traefik Mesh (formerly Maesh) is a lightweight, non-invasive service mesh built on top of Traefik Proxy for Kubernetes. It provides automatic traffic management, observability, and security for microservices without requiring sidecar containers. Traefik Mesh is compliant with the Service Mesh Interface (SMI) specification and supports HTTP, TCP, and UDP traffic modes, traffic splitting, access control via TrafficTarget, rate limiting, circuit breaking, and retries. The project is effectively dormant: the last released version is v1.4.8 (2022-08-19), and commit activity since then has been limited to CI and documentation maintenance. The GitHub repository is not formally archived as of this profile date and there is no official deprecation banner on the project's README or documentation site, but the lack of feature releases for nearly four years and the absence of an SMI-compatible successor inside Traefik Labs' product line (Traefik Hub is positioned as Kubernetes-native API management, not a service mesh) make this an unmaintained project for practical purposes.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/traefik-mesh/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/traefik-mesh/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Kubernetes
- Service Mesh
- Open Source
- SMI
- Traffic Management
- Dormant
- Unmaintained

## Timestamps

- **Created:** 2026-05-03
- **Modified:** 2026-05-23

## APIs

### Traefik Mesh Controller API

The Traefik Mesh Controller API provides internal debugging and status endpoints for the Traefik Mesh controller pod. It exposes the current dynamic configuration built by the controller, the mesh topology, the readiness status of the controller, and per-node configuration for each Traefik Mesh proxy node. The API is accessed directly on the controller pod IP at port 9000 and is not exposed via Kubernetes service for security reasons. As of the last released version (v1.4.8, 2022-08-19) this surface has not changed and is unlikely to evolve given the project's dormant maintenance state.

- **Human URL:** [https://doc.traefik.io/traefik-mesh/](https://doc.traefik.io/traefik-mesh/)
- **Base URL:** `http://controller-pod-ip:9000`

#### Tags

- Configuration
- Debugging
- Kubernetes
- Service Mesh
- Status

#### Properties

- [Documentation](https://doc.traefik.io/traefik-mesh/)
- [OpenAPI](openapi/traefik-mesh-controller-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/traefik-mesh-controller.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/traefik-mesh-controller.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [GitHub Repository](https://github.com/traefik/mesh)
- [JSON Schema](json-schema/traefik-mesh-pod-info-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/traefik-mesh-service-entry-schema.json) — [JSON Schema](https://json-schema.org/specification)

## Common Properties

- [Website](https://traefik.io/traefik-mesh)
- [Documentation](https://doc.traefik.io/traefik-mesh/)
- [GitHub Organization](https://github.com/traefik)
- [GitHub Repository](https://github.com/traefik/mesh)
- [Helm Chart](https://github.com/traefik/mesh-helm-chart)
- [Blog](https://traefik.io/blog/)
- [Community](https://community.traefik.io/)
- [Slack](https://slack.traefik.io/)
- [Terms of Service](https://traefik.io/terms/)
- [Privacy Policy](https://traefik.io/privacy/)
- [License](https://github.com/traefik/mesh/blob/master/LICENSE)
- [Spectral Rules](rules/traefik-mesh-rules.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)
- [J S O N Ld](json-ld/traefik-mesh-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Vocabulary](vocabulary/traefik-mesh-vocabulary.yml)
- [Releases](https://github.com/traefik/mesh/releases)
- [Changelog](https://github.com/traefik/mesh/releases)
- [Maintenance Status](undefined)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [L L Ms Txt](https://traefik.io/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
