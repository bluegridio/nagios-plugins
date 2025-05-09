# Nagios Plugins

This repository contains **custom Nagios plugins** developed by the **BlueGrid Platform Engineering Team** to extend monitoring capabilities for various infrastructure components.

## Available Plugins

### `check_cdn_server_heartbeat`

A Nagios-compatible plugin that checks the operational status of critical services on CDN servers.  
It verifies dependencies between services to ensure that:

- The server is fully ready for production, with all required services running, **or**
- The server is safely out of production, with critical services stopped as expected.

Specifically, it monitors:

- Host reachability (ping)
- MySQL database status (active flag)
- Routing service (Bird) status
- HTTP services (Nginx, Varnish)
- DNS resolver (Unbound) for DNS servers

Based on the combination of these checks, it reports an **OK, Warning, or Critical** state and returns the appropriate Nagios exit code.

## License

This project is licensed under the [MIT License](LICENSE).

---

Maintained by the **BlueGrid Platform Engineering Team**.