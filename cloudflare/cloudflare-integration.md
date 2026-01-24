# Cloudflare Tunnel Integration

## Setup
- Cloudflare Quick Tunnel (trycloudflare.com)
- No custom domain (dummy domain issue)
- Direct tunnel to localhost:5678

## URLs
- n8n: https://screensavers-wherever-payroll-profession.trycloudflare.com
- Webhook: https://screensavers-wherever-payroll-profession.trycloudflare.com/webhook/

## Command
```bash
cloudflared tunnel --url http://localhost:5678
```

## Status
✅ Tunnel running
✅ n8n accessible via Cloudflare
✅ Replaced ngrok with Cloudflare
