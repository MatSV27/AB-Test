# Simulador AB-100

Simulador web estático para practicar conceptos de Microsoft Copilot, Azure AI,
gobernanza, seguridad, monitoreo y despliegue.

## Estructura

```text
AB-100/
├── index.html
└── README.md
```

`index.html` es una aplicación autocontenida: incluye los estilos, la lógica y
el banco de preguntas. No requiere Node.js, servidor backend ni variables de
entorno.

## Ejecutar localmente

Abre `index.html` directamente en el navegador, o inicia un servidor estático
local desde esta carpeta:

```bash
python -m http.server 3000
```

Después visita <http://localhost:3000>.

## Desplegar en Vercel

### Desde la interfaz de Vercel

1. Sube este proyecto a un repositorio de GitHub, GitLab o Bitbucket.
2. Entra en [Vercel](https://vercel.com/new) y selecciona **Add New Project**.
3. Importa el repositorio.
4. Si Vercel solicita la carpeta del proyecto, indica `AB-100`.
5. Usa estos valores:
   - **Framework Preset:** `Other`
   - **Build Command:** déjalo vacío
   - **Output Directory:** `.`
   - **Install Command:** déjalo vacío
6. Selecciona **Deploy**.

Vercel servirá automáticamente `index.html` como página principal.

### Con Vercel CLI

Desde la carpeta `AB-100`:

```bash
npm i -g vercel
vercel
```

Para publicar en producción:

```bash
vercel --prod
```

No se necesitan configuraciones adicionales ni variables de entorno.

## Funcionalidades

- Simulacro completo y práctica por tema.
- Preguntas de opción única, múltiple y selección desplegable.
- Explicación de respuestas y tips de aprendizaje.
- Navegación entre preguntas con **Anterior**, **Siguiente** e **Inicio**.
- Recuperación de respuestas y resultados durante la navegación.
- Persistencia local de errores y último intento mediante `localStorage`.
- Diseño responsive para escritorio y dispositivos móviles.
- Soporte para preferencias de color claro y oscuro del sistema.
