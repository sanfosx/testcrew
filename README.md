# FoschiDesk CRM DevOps Plan

## 1. Estructura de Branches
### Estrategia de Branching
- **main**: Código en producción estable.
- **develop**: Código en desarrollo.
- **feature/**: Ramas para nuevas características.

### Reglas de Pull Requests
- Todo el código debe pasar las pruebas antes de ser fusionado.
- Revisión de código debe ser aprobada por al menos un colaborador.

## 2. Pipeline CI/CD
El pipeline está definido en `.github/workflows/ci-cd.yml`. Incluye lint, typecheck, tests, build, security scan y despliegue.

## 3. Configuración de Vercel
Los deployments en Vercel deben configurarse para cada environment utilizando las variables de entorno adecuadas. Las direcciones serán:
- **Development**: [your-development-url]
- **Staging**: [your-staging-url]
- **Production**: [your-production-url]

## 4. Configuración de Railway
La configuración del backend se debe hacer en Railway siguiendo la misma estrategia de ambientes:
- **Development**: [your-railway-development-url]
- **Staging**: [your-railway-staging-url]
- **Production**: [your-railway-production-url]

## 5. Administración de Variables de Entorno
Se recomienda usar herramientas como [Doppler](https://doppler.com) o [AWS Secret Manager](https://aws.amazon.com/es/secrets-manager/) para manejar las variables de entorno de manera segura.