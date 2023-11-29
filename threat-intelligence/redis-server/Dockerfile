# Use the official Redis image
FROM redis

# Expose Redis port
EXPOSE 6379

# Run Redis server with no protection mode (open to all connections)
# WARNING: This is insecure and should be used cautiously
CMD ["redis-server", "--protected-mode", "no"]
