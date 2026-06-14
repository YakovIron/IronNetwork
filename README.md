# Iron Network (IronNet)

> A private, self-hosted network for secure internal applications and services.

![IronNet Banner](./assets/banner.png)

---

## Overview

**IronNet** is a private network infrastructure designed to host and manage internal applications that are only accessible through a secured network layer or VPN connection.

It acts as a closed ecosystem where services, tools, and dashboards are exposed only to authenticated devices within the network boundary.

Think of it as a personal internal cloud — isolated, controlled, and fully under your ownership.

---

## Key Features

- 🔐 **Private Network Access Only**
  - No public exposure of internal apps
  - Access restricted via VPN / internal routing

- 🧩 **Modular App Hosting**
  - Deploy multiple internal services
  - Independent app isolation within the same network

- 🌐 **Centralized Internal Routing**
  - Single entry point for all services
  - Clean service discovery inside the network

- 🛡️ **Security First Design**
  - No direct internet-facing services (unless explicitly allowed)
  - Controlled access layers

- ⚡ **Lightweight & Scalable**
  - Designed to grow with additional services over time

---

## Architecture
```
  [ Client Devices ]
            │
            ▼
    [ VPN Gateway ]
            │
            ▼
[ IronNet Router / Core ]
           │  
    ┌──────┼──────┬───────┐
    ▼     ▼       ▼       ▼
  App 1 App 2 App 3 Internal APIs

```
  
![Network Diagram](./assets/network-diagram.png)

---

## Tech Stack (Example)

- Networking: VPN (WireGuard / OpenVPN / Tailscale-ready)
- Backend Services: Node.js / Docker containers
- Reverse Proxy: Nginx / Traefik
- Hosting: Self-hosted machine / NAS / server cluster
- Auth Layer: Token-based / network-level access control

---

## Access Model

IronNet is not publicly accessible.

To connect:

1. Join the private VPN network
2. Authenticate device access
3. Access services via internal domain routing

Example:
https://dashboard.internal
https://files.internal
https://api.internal


---

## Example Apps (Internal)

- 📊 Dashboard / Admin Panel
- 🗂️ File Storage System
- 💬 Internal Chat / Messaging
- 📡 API Services Layer
- 🧪 Experimental Apps Sandbox

---

## Project Structure
IronNet/
├── core/
│ ├── gateway/
│ ├── router/
│ └── auth/
├── services/
│ ├── dashboard/
│ ├── files/
│ └── api/
├── infra/
│ ├── docker/
│ ├── vpn/
│ └── nginx/
└── docs/



---

## Security Model

IronNet follows a **network-isolation-first** approach:

- Services are not publicly exposed
- Access requires network presence (VPN tunnel)
- Internal DNS resolves only within the network
- Optional service-level authentication for sensitive apps

---

## Future Plans

- Multi-user access control system
- Role-based permissions (RBAC)
- Service auto-discovery
- Web-based network control panel
- Encrypted internal messaging layer
- Mobile companion app

---

## Screenshots

> (Add your UI here)

![Dashboard](./assets/dashboard.png)
![Services](./assets/services.png)

---

## Status

🚧 Active development — core infrastructure evolving

---

## License

Private project — all rights reserved unless stated otherwise.
