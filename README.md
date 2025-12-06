# FreshRSS + Caddy HTTPS Gateway

## Usage

1. **Edit the Caddyfile**
   - For a domain: Replace `your.domain.com` with your domain name.
   - For IP access: Uncomment the `:443` block in the Caddyfile.

2. **Start the stack**
   ```bash
   docker compose up -d
   ```

3. **Access FreshRSS**
   - Via `https://your.domain.com` (with valid certificate from Let's Encrypt)
   - Or `https://<your-ip>` (with self-signed certificate; browser will warn)

## Certificate Management
- **Domain**: Caddy will automatically request and renew certificates from Let's Encrypt.
- **IP**: Caddy will generate a self-signed certificate for HTTPS.
- No manual certificate setup required.

## Environment Variables
- You can set FreshRSS environment variables in `docker-compose.yml` as needed.

---
For advanced Caddy configuration, see: https://caddyserver.com/docs/caddyfile
