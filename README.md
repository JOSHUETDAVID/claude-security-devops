# security-devops

Plugin de Claude Code para auditoría de seguridad y buenas prácticas DevOps.

## Skills incluidos
### `docker-audit`
Revisa tu Dockerfile antes de hacer build o deploy. Detecta problemas que
en producción se convierten en vulnerabilidades reales: imágenes corriendo
como root, secretos hardcodeados, tags sin versión fija y capas innecesarias
que inflan el peso de la imagen. Un Dockerfile mal configurado es la puerta
de entrada más común en ataques a contenedores.

### `headers-review`
Analiza los headers HTTP de tu sitio. Los headers de seguridad (CSP,
X-Frame-Options, HSTS) son la primera línea de defensa contra XSS,
clickjacking y sniffing de contenido. La mayoría de sitios en producción
los tienen mal configurados o ausentes sin saberlo.

## Instalación

```bash
git clone https://github.com/joshuet/claude-security-devops
cd claude-security-devops
cp -r skills/* ~/.claude/skills/
```

## Uso

```
/docker-audit    → pasa el path de tu Dockerfile
/headers-review  → Pasa el Contenido de tus headers
```

## Roadmap v2.0
- GitHub Actions audit
- Least privilege checker
- Cloudflare WAF integration
