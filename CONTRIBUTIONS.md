
# Contribuciones de Jharvy Cadillo

## Sprint 1

- 2025-06-22: grega el script scripts/doc_extractor.py, que permite recorrer la carpeta modules/ y extraer automáticamente información de cada módulo Terraform.

  Commits:
  - `feat(py): (Issue #3) agregar parseo de archivos .tf en los modulos` (`33331b00`)
  - `fix(sh): (Issue #3) arreglo del parse en la funcion parse_readme_md` (`5647e38`)

  Pull request grupal: [#11](https://github.com/Jharvichu/PC4_Grupo8_Proyecto10/pull/11)

- 2026-06-22: Se modifica el script doc_extractor.py para que genere automáticamente un archivo Markdown (.md) en la carpeta docs/ por cada módulo ubicado en modules/.

  Commits:
  -   `feat(py): (Issue #4) implementacion automatica de la generacion del resumen en md de los modulos` (`46cb69d`)

  Pull request grupal: [#12](https://github.com/Jharvichu/PC4_Grupo8_Proyecto10/pull/12)


## Sprint 2

- 2027-06-28: Se crea un nuevo script en scripts/diagram_generator.py y se encarga de recorrer los modulos y analizar los main.tf para extraer dependencias.

  Commits:
  - `feat(py): (Issue #14) agregar funciones de extraccion de dependencias` (`c62d7e9`)

  Pull request grupal: [#19](https://github.com/Jharvichu/PC4_Grupo8_Proyecto10/pull/19)

## Sprint 3

- 2029-06-29: Se agrega el tests `test_integration_documentation.py` para las pruebas con la documentación generada. Se documenta dicho script.

  Commits:
  - `feat(py): (Issue #24) Se implemento las pruebas de integracion` (`6ac32b4`)
  - `feat(md): (Issue #24) Documentanción las pruebas de integracion` (`bc72627`)

  Pull request grupal: [#29](https://github.com/Jharvichu/PC4_Grupo8_Proyecto10/pull/27)