# Módulo summary_creator
Ejecuta un script local que genera el archivo summary.txt con un resumen de lo creado y simula una automatización de documentación o auditoría, además es el único que no crea archivos directamente con Terraform, sino mediante un script (`local-exec` con `null_resource`); depende explícitamente de todos los demás módulos, para asegurarse de que el resumen refleje correctamente la infraestructura final.

### Tabla de variables:
| Nombre | Tipo | Descripcion | Default |
|--------|------|-------------|---------|
| root_path | string | Ruta absoluta del directorio raíz de la infraestructura. | <null> |
| config_files | list(string) | Lista de rutas de archivos de configuración generados. | <null> |
| service_name | string | Nombre lógico del servicio secundario. | <null> |
| service_path | string | Ruta absoluta del subdirectorio del servicio secundario. | <null> |
| service_file | string | Ruta del archivo de datos del servicio secundario. | <null> |
| service_data_id | string | ID del archivo de datos del servicio secundario (para dependencias explícitas). | <null> |
| depends_on_resources | list(any) | Lista de recursos de los que depende este módulo para generar el resumen. | [] |

### Tabla de outputs:
| Nombre | Descripción | Valor |
|--------|-------------|-------|
| summary_file | Ruta del archivo resumen generado por este módulo. | ${var.root_path |

### Lista de recursos:
- Recurso de tipo `null_resource` con nombre **create_summary** ejecuta el comando `echo 'Infraestructura creada en ${var.root_path}. Archivos de configuración: ${join(", ", var.config_files)}. Servicio: ${var.service_name} en ${var.service_path} con datos en ${var.service_file}' > ${var.root_path}/summary.txt` en `${var.root_path}/summary.txt`

