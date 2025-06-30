# Proyecto 10: Extractor de documentación de IaC y diagramador básico

**Alumno:** Jharvy Jonas, Cadillo Tarazona

**Código:** 20210184E

**Correo:** jharvy.cadillo.t@uni.pe

**Repositorio del Proyecto:** [https://github.com/Jharvichu/PC4_Grupo8_Proyecto10](https://github.com/Jharvichu/PC4_Grupo8_Proyecto10)

### Rol en el equipo

Para este proyecto, me encargué de la creación de algunas *issues* para cada *sprint*. Contribuí al desarrollo de los tests con el script de `python` (`test_integration_documentación.py`). Implementé también los script de `doc_extractor.py` y `diagram_generator.py` para el parseo de los archivos `.tf` y la documentacion automatica de los módulos.

### Instrucciones

Todos los comandos funcionan únicamente en sistemas basados en Linux, como Ubuntu, Debian, Fedora, etc.

```bash
$ git clone https://github.com/Jharvichu/PC4_Grupo8_Proyecto10.git
$ cd PC4_Grupo8_Proyecto10
# Entrando al entorno de trabajo
$ source setup.sh
# Generar documentacion
$ python3 scripts/doc_extrator.py
$ python3 script/diagram_generator.py
# Probando los tests (Ahi esta incluido test_integration_documentation)
$ pytest
```

> NOTA: los módulos terraform dentro de `infra/modules/` son necesarios para probar los tests, es por eso que se agregan al repositorio.
> Los archivos markdown dentro de `docs/` son generados, por lo cual no tienen una autoría definida. 