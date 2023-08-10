# Reverse Proxy with NGINX

This repository contains the necessary Docker configuration files to set up a reverse proxy using Nginx, which will receive HTTPS requests from one domain and redirect them to another domain.

## Getting Started

1. Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/reverse-proxy.git
cd reverse-proxy
```

2. Replace the placeholders in the configuration files with your actual domain and SSL certificate information.

3. Place your SSL certificate (`yourdomain.crt`) and private key (`yourdomain.key`) in the `ssl` directory.

4. Build and run the Docker container:

```bash
docker-compose up -d
```

## Configuration

### `nginx.conf`

The `nginx.conf` file contains the base configuration for the Nginx server. It uses the `http` module to handle SSL termination and proxying to the backend server.
## Important Notes

- Make sure you have valid SSL certificates for both your source and destination domains.
- Adjust the proxy headers as needed to pass relevant client information to the backend server.