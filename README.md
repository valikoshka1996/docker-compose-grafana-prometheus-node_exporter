### How this script works:
- **Installs Docker**: Updates system packages, adds the Docker repository, installs Docker, and adds the user to the Docker group.
- **Installs Docker Compose**: Downloads and installs the latest version of Docker Compose.
- **Creates a `docker-compose.yml` file**: Describes the configuration for Grafana, Prometheus, and Node Exporter.
- **Creates the `prometheus.yml` configuration file**: Configures Prometheus to scrape metrics from itself and Node Exporter.
- **Runs Docker Compose**: Starts all services in containers.

### Execution:
1. Save the script to a file, for example, `install.sh`.
2. Make the file executable:
   ```bash
   chmod +x install.sh
3. Run script
   `./install.sh`
After running the script, the monitoring system will be available on the following ports:

Prometheus: http://localhost:9090

Grafana: http://localhost:3000 (Login: admin, Password: admin)

When adding a new datasource - Prometheus - in the host field, specify: http://prometheus:9090.
