# Nextcloud-as-a-Service Project

Deploy a functional and secure Nextcloud collaborative server on Kubernetes with custom manifests and Docker images.

# Prerequisites

- Nextcloud web folder is prepared with correct permissions.

- A functional NFS server accessible on the network.

- Shared NFS folders are accessible with correct permissions (the UID of the nginx user must match across containers).

- Kubernetes cluster with Ingress and a CNI installed.

- Access to an external container image registry.

- UID and GID of the web user must be consistent for nginx and PHP containers and align with NFS folder permissions.

Configuration Variables

ConfigMap:
PHP_SERVICE:PHP_PORT
NGINX_PORT
HOSTNAME
REDIS_SERVER
REDIS_PORT
REDIS_PASSWORD
REDIS_DATABASE

Miscellaneous
REGISTRY_CREDENTIALS
REGISTRY_KEY
MY_SECRETS
NAMESPACE

Storage
WEBPVC
DATAPVC
NFS_SERVER
NFS_SERVER_WORKDIR

Ingress
HOSTNAME
TLS_CERTIFICATE
CRT_PUBLIC_KEY
CRT_PRIVATE_KEY

Nginx
NGINX_PORT
NGINX_SERVICE
NGINX_DEPLOYMENT
NGINX_IMAGE

PHP
NGINX_USER
PHP_SERVICE
PHP_DEPLOYMENT
PHP_PORT
PHP-FPM_IMAGE

MariaDB
MARIADB_SERVICE
MARIADB_PORT

Redis
REDIS_SERVICE
REDIS_DEPLOYMENT
REDIS_PORT