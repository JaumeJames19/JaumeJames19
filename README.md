### Hola, soy Jaume 👋

Monto y mantengo la infraestructura de casa y algunas herramientas para el
trabajo como si fueran proyectos de verdad: con git, revisión, tests,
integración continua y despliegue automático. Casi todo lo trabajo junto con
[Claude Code](https://claude.com/claude-code), con hooks, subagentes y reglas
propias en cada repositorio.

Los repositorios son privados porque describen mi casa y mi red. Esto es lo
que hay dentro.

#### 🏠 Domótica (Home Assistant)

- La configuración entera en YAML, organizada en paquetes por función: clima,
  persianas, iluminación, seguridad, energía…
- **Unos 600 tests con pytest** y un contrato de referencias que detecta
  entidades rotas antes de desplegar.
- La CI valida la configuración contra Home Assistant `stable` en cada PR, y
  contra `beta` y `dev` cada semana. pre-commit con yamllint, prettier,
  actionlint y zizmor.
- Despliegue solo por git: al fusionar a `master`, el equipo se actualiza
  solo.

#### 🗄️ Homelab (NAS con Docker)

- Unos 30 servicios en Docker Compose, cada uno con su documentación:
  fotos, contraseñas, vídeo vigilancia, automatización, monitorización…
- **GitOps:** al fusionar a `main`, un script lo trae al NAS y redespliega
  solo lo que ha cambiado.
- Renovate para las versiones (nunca `:latest`), Trivy para las imágenes y
  shellcheck para los scripts.
- Entrada por Tailscale con política de acceso, Caddy y Authelia (SSO con
  doble factor), y un proxy de Docker de mínimos permisos para los agentes de
  IA.

#### ⏱️ Registro de jornada

App web para fichar en una empresa: PIN con bloqueo por fuerza bruta,
doble factor para los encargados, fichajes que no se pueden modificar (las
correcciones se aprueban y quedan auditadas), cálculo de horas según el
convenio y exportación para la gestoría.

#### 🧰 Con qué trabajo

`Home Assistant` · `ESPHome` · `Docker` · `Tailscale` · `Caddy` · `Authelia` ·
`n8n` · `GitHub Actions` · `Python` · `TypeScript` · `React` · `Supabase` ·
`Claude Code`
