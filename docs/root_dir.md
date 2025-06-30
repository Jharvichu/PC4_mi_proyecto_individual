# Módulo root_dir
Crea el directorio raíz de toda la infraestructura local: infra_local/ y además es
practicamente la base; los demás (archivos, subdirectorios, scripts) se construyen 
dentro de este directorio.

### Tabla de variables:
| Nombre | Tipo | Descripcion | Default |
|--------|------|-------------|---------|
| root_name | string | Nombre lógico del directorio raíz de la infraestructura local. | infra_local |
| root_path | string | Ruta absoluta donde se creará el directorio raíz. | <null> |

### Tabla de outputs:
| Nombre | Descripción | Valor |
|--------|-------------|-------|
| root_path | Ruta absoluta del directorio raíz creado por este módulo. | var.root_path |
| root_name | Nombre lógico del directorio raíz creado por este módulo. | var.root_name |

### Lista de recursos:
- Recurso de tipo `local_file` con nombre **keep_root** crea el archivo `${var.root_path}/.keep` con contenido `Directorio raíz de la infraestructura local: ${var.root_name}`

