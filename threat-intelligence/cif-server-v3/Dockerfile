# Use the base CIF server image
#FROM renisac/cifv3
FROM renisac/cifv3-cligit 
# Set the working directory
WORKDIR /home/cif

# Create the .cif.yml configuration file
RUN echo "" > .cif.yml

# Set file permissions
RUN chmod 644 /home/cif/.cif.yml

