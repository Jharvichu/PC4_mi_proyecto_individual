# Módulo config_files
Genera archivos de configuración (main.conf, app.conf) dentro del directorio raíz y además
requiere que root_dir haya creado correctamente su estructura.

### Tabla de variables:
| Nombre | Tipo | Descripcion | Default |
|--------|------|-------------|---------|
| root_path | string | Ruta absoluta del directorio raíz donde se crearán los archivos de configuración. | <null> |
| project_name | string | Nombre del proyecto para contextualizar los archivos de configuración. | infra_local |
| depends_on_resource | any | Recurso del que depende la creación de los archivos de configuración (generalmente el directorio raíz). | <null> |

### Tabla de outputs:
| Nombre | Descripción | Valor |
|--------|-------------|-------|
| config_files | Lista de rutas de los archivos de configuración generados por este módulo. | [ |
| config_files_ids | IDs de los recursos de archivos de configuración generados (para dependencias). | [ |

### Lista de recursos:
- Recurso de tipo `local_file` con nombre **config1** crea el archivo `${var.root_path}/main.conf` con contenido `Archivo de configuración principal para ${var.project_name}.`
- Recurso de tipo `local_file` con nombre **config2** crea el archivo `${var.root_path}/app.conf` con contenido `Archivo de configuración secundaria para ${var.project_name}.`

