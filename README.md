# Unraid Integration for Home Assistant

This custom integration allows you to monitor and control your Unraid server from Home Assistant. Unraid is a popular NAS (Network Attached Storage) operating system that provides flexible storage, virtualization, and application support.

## Development Status

This integration is in active development. Here are a few things to keep in mind:

- Features may be added, changed, or removed without notice.
- There might be bugs or unexpected behavior.
- Regular updates may be necessary as the integration evolves.
- Feedback and contributions are welcome to help improve the integration.

## Features

- Monitor CPU, RAM, Boot, Cache, Array Disks, and Array usage
- Monitor CPU and Motherboard temperature
- Monitor UPS connected
- Control Docker containers
- Control VMs
- Execute shell commands
- Manage user scripts

## Installation

### HACS (Recommended)

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=domalab&repository=ha-unraid&category=integration)

### Manual

1. Copy the `unraid` folder into your `custom_components` directory.
2. Restart Home Assistant.
3. Go to Configuration > Integrations.
4. Click the "+ ADD INTEGRATION" button.
5. Search for "Unraid" and select it.
6. Follow the configuration steps.

## Configuration

During the setup, you'll need to provide:

- Host: The IP address or hostname of your Unraid server
- Username: Your Unraid username (usually 'root')
- Password: Your Unraid password
- Port: SSH port (usually 22)
- Ping Interval: How often to check if the server is online (in seconds). Default is 60 seconds.
- Update Interval: How often to update sensor data (in seconds). Default is 300 seconds.

Note: Setting lower intervals will provide more up-to-date information but may increase system load.

## Sensors

- CPU Usage: Shows the current CPU utilization percentage.
- RAM Usage: Displays the current RAM usage percentage.
- CPU and Motherboard Temps: Shows CPU and Motherboard temperatures
- Array Usage: Shows the overall array usage percentage.
- Individual Array Disks: Displays usage information for each disk in the array.
- Uptime: Shows how long the Unraid server has been running.
- UPS Status: Displays information about the connected UPS (if available).

## Switches

- Docker Containers: Turn on/off Docker containers
- VMs: Turn on/off Virtual Machines

## Services

- `unraid.execute_command`: Execute a shell command on the Unraid server
- `unraid.execute_in_container`: Execute a command in a Docker container
- `unraid.execute_user_script`: Execute a user script
- `unraid.stop_user_script`: Stop a running user script

## Contributing

Contributions to this integration are welcome. Please fork the repository and submit a pull request with your changes. Make sure to follow the contribution guidelines.

## License

This integration is released under the Apache License.

## Disclaimer

This integration is not officially associated with or endorsed by UNRAID. UNRAID trademarks belong to UNRAID, and this integration is independently developed.