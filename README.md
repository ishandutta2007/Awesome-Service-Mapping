# Awesome-Service-Mapping

# Top Service Mapping Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Application Dependency Mapping, CMDB Topology & Service Impact Analysis*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Service Mapping**. These tools automatically discover and visualize the relationships between business services and their underlying IT components—applications, servers, databases, network devices, and cloud resources—enabling faster root cause analysis, informed change management, and accurate impact assessment.

**Examples** include ServiceNow Service Mapping, Device42, Virima, BMC Helix Discovery, Dynatrace, Datadog Service Map, ScienceLogic SL1, SolarWinds Server & Application Monitor, New Relic Service Map, and AppDynamics Service Map (the category leaders).

**Open-source emphasis**: This section is expanded with active projects for self-hosted CMDB, dependency graphing, and service catalog tooling—ideal for organizations building sovereign service mapping infrastructure without per-node licensing lock-in.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[ServiceNow Service Mapping](https://www.servicenow.com/)**  
  Automated service mapping with three approaches: Tag-Based mapping for cloud-native services (fastest time-to-value), ML-Based mapping using Predictive Intelligence for custom applications, and traditional Top-Down mapping for legacy on-premise COTS applications; integrates with CMDB and Event Management for impact analysis and root cause identification .

- **[Device42](https://www.device42.com/)**  
  Agentless discovery and dependency mapping platform (acquired by Freshworks in 2024) providing full visibility into hybrid IT estates including applications, software, network devices, containers, and cloud resources; Application Dependency Mapping (ADM) discovers running services and imports detailed configuration data, with resource maps for exploring relationships .

- **[Virima](https://virima.com/)**  
  ITAM/ITSM SaaS platform with Services Topology View that identifies underlying IT components and connectivity between web servers, application servers, middleware, and databases; provides visual impact analysis for change management and outage response, with ESXi host discovery for virtualized environments .

- **[BMC Helix Discovery](https://www.bmc.com/)**  
  Service modeling with blueprints—predefined service templates with static or dynamic rules—that visually map service processes; supports node kinds (Host, Software Instance) with relationships, and integrates with BMC Helix AIOps for service health monitoring and impact analysis .

- **[Dynatrace](https://www.dynatrace.com/)**  
  Service Map with single-screen interactive topology that automatically discovers runtime connections (upstream callers, downstream dependencies, database queries, messaging flows) and overlays live health and performance data; supports zoom, search, isolation of nodes, and drill-down to traces and logs without context switching .

- **[Datadog Service Map](https://www.datadoghq.com/)**  
  Service map visualization widget that displays all services calling and called by a given service; integrates with APM and infrastructure monitoring for dependency-aware troubleshooting .

- **[ScienceLogic SL1 (Skylar One)](https://sciencelogic.com/)**  
  Service-centric operations platform with Layer 2 and Layer 3 relationship discovery, including Linux servers, cloud edges, and non-network endpoints; Juneau release adds Geographic Maps for real-world operational context and improved dependency accuracy even when only one side of a connection reports data .

- **[SolarWinds Server & Application Monitor](https://www.solarwinds.com/)**  
  Application Dependency polling discovers and monitors TCP connections between applications and application processes using deployed agents; includes Connection Quality polling for latency and packet loss metrics, with troubleshooting guidance for agent deployment .

- **[New Relic Service Map](https://newrelic.com/)**  
  Visual representation of interconnected components from frontend to backend, dynamically showing relationships between applications, databases, hosts, and external services; works with distributed tracing and supports relationship depth filtering (depth 1-3) to focus on degraded entities .

- **[AppDynamics Service Map](https://www.appdynamics.com/)**  
  Interactive Services topology flow map showing how services interact with each other and external systems; arrow direction indicates data flow, and the view changes based on selected time range, with List/Map toggle for context preservation .

## Open-Source GitHub Projects

- **[Atlas CMDB](https://github.com/mojoaar/atlascmdb)**  
  Open-source CMDB built on Next.js (MIT-licensed) for modern IT teams; manages services, applications, CIs, assets, teams, and relationships in one place; features interactive relationship graphs with BFS depth control (1–6 hops) and Dagre auto-layout, rack management, geographic maps via Leaflet, CSV import/export, SSO (OIDC PKCE), SCIM 2.0 provisioning, TOTP MFA, and audit trail with before/after diffs .

- **[iTop](https://github.com/Combodo/iTop)**  
  Open-source IT service management platform and CMDB written in PHP; combines ITIL-aligned ticketing with a full CMDB covering servers, VMs, storage, network devices, applications, contacts, and contracts; impact analysis is rendered graphically through GraphViz, showing which services and customers are affected by a CI outage; includes a documented REST API for integration .

- **[Backstage](https://github.com/backstage/backstage)**  
  Open-source software catalog and internal developer portal from Spotify, maintained by CNCF; ingests data from integrated services and organizes it into a standardized metadata repository; the software catalog is a core feature, though visualizing dependencies requires frontend React customization .

- **[Imbi](https://github.com/AWeber-Imbi/imbi-api)**  
  DevOps Service Management Platform (v2.0 alpha) for managing complex service ecosystems; uses Apache AGE (PostgreSQL graph extension) for dependency modeling and relationship visualization; provides complete service inventory with ownership, health scoring, and links to repos/CI/CD/monitoring; API-first with OAuth2/OIDC and fine-grained authorization .

- **[NetBox Services Plugin](https://github.com/...) / netbox-services**  
  Plugin extending NetBox to manage and relate business services to network resources; introduces a Service model for tracking service types (L2VPN, L3VPN, DIA, CDN, Voice) and associating them with devices, interfaces, cables, VLANs, prefixes, VRFs, ASNs, tunnels, and VMs; provides a true service-centric view of the network beyond simple tagging .

- **[Zabbix Service Monitoring](https://www.zabbix.com/)**  
  Built-in service tree functionality for business-level monitoring; creates a hierarchy of parent/child services with status calculation rules, problem tag mapping, and SLA tracking; status propagates upward according to configurable rules, enabling service-level impact visibility from underlying infrastructure problems .

### Additional Strong Open-Source Options

- **Mercator** — Open-source CMDB and cartography tool oriented toward security and ANSSI compliance (French); models dependencies across application, logical server, physical server, and network layers; can consume data from GLPI or ServiceNow for discovery; complements ITSM-focused CMDBs with security-oriented service mapping .
- **GLPI with GraphViz** — Open-source ITSM and asset management platform with impact analysis visualization; widely used as a discovery source for other mapping tools.
- **ArchMAP / Archiviz** — Static code architecture analysis tools that build dependency graphs from source code; useful for application-level mapping within DevOps workflows .

**Frameworks for building custom systems**: Combine **Atlas CMDB** for modern web-based CMDB with interactive relationship graphs, **iTop** for ITIL-aligned service mapping with GraphViz impact analysis, **NetBox Services** for network-centric service modeling, and **Zabbix Service Monitoring** for SLA-driven service trees in a fully self-hosted service mapping stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Service mapping platforms handling infrastructure data must comply with applicable security and privacy regulations; topology data can reveal sensitive architecture details.
- Self-hosted open-source solutions require proper discovery agent deployment, credential management, and CMDB data quality governance.
- Verify license terms for commercial use; Atlas CMDB uses MIT, iTop uses AGPL-3.0, Backstage uses Apache 2.0, and NetBox Services uses MIT.

---

**Made for IT operations teams, SREs, enterprise architects, and CMDB administrators.**  
Let's make service mapping more open, accurate, and impact-aware.
