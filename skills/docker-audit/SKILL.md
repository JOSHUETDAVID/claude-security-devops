---
name: docker-audit
description: Auditing Dockerfiles for security, size and best practices.
---

When auditing a Dockerfile, check for:
1. Base image uses a specific tag, not `latest`. Official slim/alpine variant preferred.
2. Multi-stage build present to separate build and runtime layers.
3. Application runs as non-root user (useradd + USER directive before CMD).
4. No hardcoded secrets, tokens or passwords in ENV or ARG instructions.
5. Package managers use no-cache flags (--no-cache-dir for pip, --no-cache for apk).
6. `.dockerignore` exists and excludes in every case of the example programming language: .env, __pycache__, .git, *.pyc, venv/.
7. Only necessary ports are exposed with EXPOSE.
8. COPY is specific (not COPY . .) unless .dockerignore is confirmed complete.
