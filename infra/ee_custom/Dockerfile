# Gunakan EE default AWX sebagai base
FROM quay.io/ansible/awx-ee:latest

# Switch ke root untuk install collection
USER root

# Install PostgreSQL collection
RUN ansible-galaxy collection install community.postgresql

# Kembali ke default user AWX
USER 1001

