
# Stingar Capabilities Deployment Repository

This repository hosts all the necessary artifacts for deploying the basic capabilities of Stingar: honeypots, threat intelligence, and blocking. Each of these capabilities is organized into separate subfolders, each containing its own `docker-compose` file.

## Deployment Instructions

To deploy any of the Stingar components, follow these steps:

1. **Navigate to the Component Folder**: Choose the capability you want to deploy (honeypots, threat intelligence, or blocking) and navigate to the corresponding subfolder.

2. **Use Docker-Compose**: Within each subfolder, you'll find a `docker-compose` file. Use this file to deploy the component.

## Component Details

### Honeypots
- A sample honeypot configuration is provided. However, the final configuration should be completed through the UI in the CHN server.

### Threat Intelligence
- **Note**: The configuration for threat intelligence is currently incomplete due to integration conflicts. This component may not function as expected until these issues are resolved.

### Blocking
- Instructions for deploying the blocking capability are provided in the corresponding subfolder.

## Additional Information

For more detailed instructions on configuration and deployment, refer to the README files located within each component's subfolder.

---

This revised README provides a clear introduction to what the repository contains, followed by structured sections for deployment instructions and specific details about each component. This structure should make it easier for users to understand and follow the deployment process.



### Starting the each Cluster

1. **Navigate to Your Project Directory**: Open a terminal and navigate to the directory where your `docker-compose.yml` file is located.

2. **Start the Cluster**: Run the following command to start all services defined in your Docker Compose file:

docker-compose up

This will start all the services (containers) defined in your `docker-compose.yml` file. If you want to run the containers in the background, add the `-d` flag:

docker-compose up -d

### Starting a Specific Service

If you want to start only a specific service (node) from your Docker Compose file, you can do so by specifying the service name after the `up` command:

docker-compose up -d [service_name]

Replace `[service_name]` with the name of the service you want to start. For example, if you want to start only the `chn-server` service, you would run:


docker-compose up -d chn-server


This command will start the `chn-server` service and any other services it depends on as defined in your Docker Compose file.

### Notes

- **Dependencies**: Docker Compose automatically starts services in dependency order. If a service depends on another service (defined using `depends_on` in your Docker Compose file), Docker Compose will start the dependencies first.
- **Logs**: To follow the logs of your services, omit the `-d` flag from the `docker-compose up` command.
- **Troubleshooting**: If your services are not starting as expected, use `docker-compose logs [service_name]` to check the logs for any service. This can provide insights into any issues or errors preventing the service from starting correctly.
- **Stopping Services**: To stop the services, use `docker-compose down`. This command stops and removes any containers, networks, volumes, and images created by `docker-compose up`.
