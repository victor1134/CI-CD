# Pipeline CI/CD para Microservicios con AKS + GitHub Actions

Este proyecto implementa una arquitectura CI/CD completa usando:

- GitHub Actions (CI + CD)
- Docker
- Azure Container Registry (ACR)
- Azure Kubernetes Service (AKS)
- Microservicios (API + Worker)

## Arquitectura

Commit → GitHub Actions CI → ACR → GitHub Actions CD → AKS

## Microservicios
### API
Servicio HTTP básico en Flask.

### Worker
Proceso en segundo plano que imprime logs cada 5 segundos.

## CI (build & push)
El workflow `ci.yml`:
- Construye imágenes
- Corre pruebas (opcional)
- Hace push a ACR

## CD (deploy)
El workflow `cd.yml`:
- Obtiene credenciales del cluster
- Aplica manifestos Kubernetes automáticos

## Despliegue
Para ver servicios:

