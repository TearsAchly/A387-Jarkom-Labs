# Node.js Express App with Nginx Reverse Proxy Configuration

This repository contains a simple Node.js Express application configured with Nginx as a reverse proxy.

## Prerequisites

- Node.js installed on your system
- Nginx installed on your system
- Basic understanding of Node.js and Nginx configurations

## Project Structure

- `app.js`: Entry point of the Node.js Express application.
- `package.json`: Contains project metadata and dependencies.
- `nginx.conf`: Nginx configuration file for reverse proxy setup.

## Getting Started

1. **Clone the repository:**

   ```bash
   git clone https://github.com/TearsAchly/A387-Jarkom-Labs.git
   cd A387-Jarkom-Labs
   ```

2. **Install Dependencies:**

   ```bash
   npm install
   ```

3. **Start the Node.js Application:**

   ```bash
   npm start
   ```

   This command will start the Node.js application on `http://localhost:8000`.

4. **Configure Nginx:**

   Edit your Nginx configuration file (`nginx.conf`) and add or replace the contents with the provided configuration to set up a reverse proxy for your Node.js application.

5. **Restart Nginx:**

   After configuring Nginx, restart the Nginx service to apply the changes.

   ```bash
   sudo systemctl restart nginx
   ```

6. **Access Your Application:**

   Open a web browser and navigate to `http://localhost:3000`. Nginx will reverse proxy requests to the Node.js application running on port 8000.

## Nginx Configuration Details

The Nginx configuration (`nginx.conf`) includes:

- `limit_req_zone`: Rate limiting configuration to limit requests per IP address.
- Proxy settings to pass requests from Nginx to the Node.js application:
  - `proxy_pass`: Specifies the URL of the proxied server.
  - `proxy_set_header`: Sets headers passed to the proxied server.

## Additional Notes

- Ensure that both Node.js and Nginx are properly installed and configured on your system.
- Customize the Nginx configuration based on your application's requirements (e.g., SSL settings, gzip compression).
- For production deployments, consider security best practices and monitoring configurations.

## License

This project is licensed under the MIT license. See the [LICENSE](LICENSE) file for more information.
