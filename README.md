# Self-hosted RSS reader

Self-host [FreshRSS](https://freshrss.org/), a RSS reader with a web interface, with Docker. Serves over secure HTTPS.

## Installation

1. Check out this repository
`git clone https://github.com/ggeorgovassilis/selfhosted-reader`

2. Create an .env file with this content:
```
DOMAIN=your.domain
PORT=443
```

3. (Set up the domain DNS to point to your server)

4. `docker compose up -d`
   
5. **Access FreshRSS**
   - Via `https://your.domain:port` (with valid certificate from Let's Encrypt)
   - Or `https://<your-ip>:port` (with self-signed certificate; browser will warn)
Follow the wizard instruction to set up a user name and password.

## Certificate Management
- **Domain**: Caddy will automatically request and renew certificates from Let's Encrypt.
- **IP**: Caddy will generate a self-signed certificate for HTTPS.
- No manual certificate setup required.

## Environment Variables
Edit variables in .env
