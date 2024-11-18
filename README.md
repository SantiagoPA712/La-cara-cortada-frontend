# La Cara Cortada - Frontend

Este es el frontend de la aplicación **La Cara Cortada**, desarrollado en React. La aplicación interactúa con un backend basado en NestJS y permite a los usuarios explorar modelos, productos de maquillaje, eventos de moda, fotos, y membresías exclusivas.

---

## **Características Principales**

- **Autenticación de Usuario**:
  - Inicio de sesión con JWT.
  - Rutas protegidas mediante `PrivateRoute`.

- **Interfaz de Usuario**:
  - Navegación intuitiva con rutas para modelos, productos, eventos, fotos y membresías.
  - Interfaz responsiva para dispositivos móviles y de escritorio.
  - Estilos básicos aplicados con CSS.

- **Consumo de API**:
  - Comunicación con el backend mediante Axios.

---

## **Requisitos Previos**

### **Software Necesario**
- **Node.js** (v16 o superior)
- **npm** (incluido con Node.js)

---

## **Instalación**

1. Clona el repositorio:
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   cd frontend
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Configura las variables de entorno:
   Crea un archivo `.env` en el directorio raíz y agrega la URL del backend:
   ```plaintext
   REACT_APP_API_URL=http://localhost:3000/api
   ```

4. Inicia el servidor de desarrollo:
   ```bash
   npm start
   ```

5. Abre la aplicación en tu navegador:
   ```plaintext
   http://localhost:3000
   ```

---

## **Estructura del Proyecto (Principal)**

```plaintext
frontend/
├── src/
│   ├── components/         # Componentes reutilizables (Navbar, PrivateRoute)
│   ├── pages/              # Páginas principales (Home, Login, Models, etc.)
│   ├── services/           # Lógica de conexión con la API (Axios)
│   ├── App.tsx             # Punto de entrada principal de React
│   ├── routes.tsx          # Configuración de rutas
├── public/                 # Archivos estáticos
├── .env                    # Variables de entorno
├── package.json            # Dependencias y scripts
```

---

## **Páginas Disponibles**

### **Rutas Principales**

| Ruta                | Descripción                          |
|---------------------|--------------------------------------|
| `/`                 | Página de inicio                    |
| `/login`            | Inicio de sesión                    |
| `/models`           | Listado de modelos                  |
| `/products`         | Listado de productos de maquillaje  |
| `/events`           | Listado de eventos de moda          |
| `/photos`           | Galería de fotos para la venta      |
| `/memberships`      | Detalles de membresías exclusivas   |
| `/dashboard`        | Panel de administración (privado)   |

---

## **Consumo de API**

El frontend consume las siguientes rutas de la API:

- **Usuarios:**
  - `POST /auth/login`: Para autenticar usuarios.
- **Modelos:**
  - `GET /models`: Obtiene todos los modelos.
- **Productos:**
  - `GET /products`: Lista los productos disponibles.
- **Eventos:**
  - `GET /events`: Lista los eventos disponibles.

---

## **Pruebas**

Para asegurarte de que el frontend funciona correctamente:

1. Inicia el backend en el puerto `3000`:
   ```bash
   npm run start:dev
   ```

2. Inicia el frontend en el puerto `3000`:
   ```bash
   npm start
   ```

3. Navega a la página principal y prueba las siguientes funcionalidades:
   - Inicio de sesión con credenciales válidas.
   - Navegación por todas las páginas disponibles.
   - Verificación de rutas protegidas.

---

## **Despliegue**

1. Construye la aplicación:
   ```bash
   npm run build
   ```

2. Despliega en una plataforma como Vercel o Netlify:
   - Para Vercel:
     ```bash
     npx vercel
     ```
   - Para Netlify, sube la carpeta `build` al dashboard.

3. Configura la variable `REACT_APP_API_URL` en el entorno de producción.

---

## **Licencia**

Este proyecto es ficticio y no está destinado para uso comercial.
