# Sistema de Gestión de Contratos - SECOP II

Sistema web para la gestión de contratos públicos integrado con SECOP II (Sistema Electrónico para la Contratación Pública).

## Descripción

Este proyecto es una aplicación web que permite a los usuarios autenticados gestionar y consultar información de contratos públicos. El sistema incluye autenticación mediante correo electrónico, selección de entidades y un panel de administración completo.

## Características

- **Autenticación simplificada**: Login mediante correo electrónico sin contraseña visible (encriptada en backend)
- **Selección de entidad**: Los usuarios pueden seleccionar entre múltiples entidades asociadas
- **Panel de administración**: Visualización y gestión de contratos con tabla interactiva
- **Búsqueda avanzada**: Sistema de búsqueda de contratos con filtros
- **Carga de documentos**: Funcionalidad para subir documentos relacionados con contratos
- **Diseño responsive**: Compatible con dispositivos móviles, tablets y desktop

## Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **Tailwind CSS**: Framework de estilos y diseño responsive
- **JavaScript (ES6+)**: Lógica del frontend
- **SessionStorage**: Manejo de sesiones del lado del cliente

## Estructura del Proyecto

```
.
├── img/
│   └── logo-2024-png.png       # Logo de la aplicación
├── login.html                   # Página de inicio de sesión
├── seleccion-entidad.html      # Página de selección de entidad
├── panel-admin.html            # Panel de administración principal
└── README.md                    # Documentación del proyecto
```

## Instalación y Uso

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/Unravel56/contingencia.git
   cd contingencia
   ```

2. **Abrir en navegador**
   - Simplemente abra el archivo `login.html` en su navegador web
   - No requiere servidor local (por ahora es frontend estático)

3. **Navegación**
   - Ingrese cualquier correo electrónico válido en el login
   - Seleccione una entidad de la lista
   - Acceda al panel de administración

## Flujo de la Aplicación

1. **Login** (`login.html`)
   - Usuario ingresa su correo electrónico
   - Sistema simula validación con Stored Procedure
   - Redirección automática a selección de entidad

2. **Selección de Entidad** (`seleccion-entidad.html`)
   - Usuario selecciona la entidad con la que desea trabajar
   - Se guarda la información en sessionStorage
   - Redirección al panel de administración

3. **Panel de Administración** (`panel-admin.html`)
   - Visualización de contratos en tabla
   - Búsqueda y filtrado de contratos
   - Carga de documentos
   - Paginación de resultados

## Configuración de Colores

El proyecto utiliza el siguiente esquema de colores:
- **Color principal**: `#233a79` (Azul institucional)
- **Tema**: Light (fondo blanco)

## Próximas Implementaciones

- [ ] Integración con backend y base de datos
- [ ] Implementación real de Stored Procedures
- [ ] Sistema de autenticación robusto
- [ ] API REST para operaciones CRUD
- [ ] Exportación de datos a Excel/PDF
- [ ] Notificaciones en tiempo real
- [ ] Dashboard con estadísticas

## Notas de Desarrollo

- La autenticación actual es simulada para propósitos de desarrollo
- En producción, reemplazar la función `simulateStoredProcedure()` con llamadas reales al backend
- Los Stored Procedures manejarán la lógica de autenticación y validación en el servidor
- La contraseña se maneja encriptada en el backend (no se solicita en el frontend)

## Autor

Desarrollo realizado para la gestión de contratos públicos según lineamientos de SECOP II.

## Licencia

Proyecto privado - Todos los derechos reservados © 2025
