# Self-hosted RSS reader

NOT READY FOR USE YET!!!

## What is this?

A self-hosted RSS reader with a web interface, serving over HTTPS


## Installation

1. Check out this repository
`git clone https://github.com/ggeorgovassilis/selfhosted-reader`

2. Create an .env file with this content:
DOMAIN=your.domain

3. (Set up the domain DNS to point to your server)

4. `docker compose up -d`
   
5. **Access FreshRSS**
   - Via `https://your.domain.com` (with valid certificate from Let's Encrypt)
   - Or `https://<your-ip>` (with self-signed certificate; browser will warn)
Follow the wizard instruction to set up a user name and password.

## Certificate Management
- **Domain**: Caddy will automatically request and renew certificates from Let's Encrypt.
- **IP**: Caddy will generate a self-signed certificate for HTTPS.
- No manual certificate setup required.

## Environment Variables
Edit variables in .env
