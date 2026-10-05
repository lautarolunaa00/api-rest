# API REST de autenticación

Backend de práctica con Express, MongoDB, Mongoose y Nodemailer.

## Requisitos

- Node.js 20.6 o superior
- pnpm
- MongoDB local en `127.0.0.1:27017`

## Instalación y ejecución

```bash
pnpm install
pnpm dev
```

`pnpm dev` carga `.env` automáticamente y reinicia el servidor al detectar cambios. Para iniciar sin modo desarrollo, usa `pnpm start`.

Crea un archivo `.env` en la raíz con la configuración de correo:

```dotenv
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=tu-correo@gmail.com
EMAIL_PASS=tu-clave-de-aplicacion
EMAIL_FROM=tu-correo@gmail.com
```

No subas `.env` a GitHub. La conexión actual a MongoDB está definida en `src/config/database.js`.

## Rutas

Todas usan el prefijo `/api/auth`:

- `POST /register`: crea un usuario y envía un código por correo.
- `POST /login`: en desarrollo; todavía no completa la autenticación.
- `GET /`: lista usuarios solo para pruebas locales. No la expongas públicamente.

La verificación del código aún no está implementada.
