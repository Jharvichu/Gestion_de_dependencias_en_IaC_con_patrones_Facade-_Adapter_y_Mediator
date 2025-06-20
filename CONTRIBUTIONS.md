# Contribuciones de Jharvy Jonas Cadillo Tarazona

## Sprint 1

- 2025-06-08: Cree la primera version del script principal `run_all.sh` que primeramente ejecutaba  el paso *adaper* y el script `generar_dependencies.py` que generaba un *JSON* estatico de las dependencias.  
  
  Commit:
  -	`feat(sh): (Issue #6) crear archivo run_all.sh inicial con el step adapter`
  - `feat(py): (Issue #6) agregar script generar_dependencies.py para crear dependencies.json inicial`

  Pull request grupal: [#11](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/11)

- 2025-06-10: Se crea la carpeta `test` y se añadio una prueba básica `test_adapter_output.py` para validar la salida JSON de `adapter_output.py`, ademas de crear el archivo `pytest.ini` para la configuracion del test. 
  
  Commit:
  -	`test(py): (Issue #7) prueba basica para validar salida JSON y configuración inicial de cobertura` (`706217`)
  -	`docs(readme): (Issue #7) agregar documentación inicial sobre pruebas` (`8d49232`)

  Pull request grupal: [#13](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/13)

## Sprint 2

- 2025-06-15: Se mejoro `generar_dependencies.py` para analizar dinámicamente las dependencias entre módulos y recursos de Terraform, actualizando automáticamente dependencies.json con las dependencias detectadas. Se añadieron expresiones regulares para identificar dependencias reales (no solo adapter y facade).

  Commits:
  - `feat(py): (Issue #19) refactorizacion del script generar_dependencies.py para la generacion de dependencias dinamicas` (`6132774`)
  - `docs(readme): (Issue #19) agregar documentacion de la mejora del script generar_dependencies.py` (`f4009c6`)

  Pull request grupal: [#33](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/33)

- 2025-06-15: Se mejoro la función run_terraform() para que pueda recibir el parámetro de variables para terraform y se implemento los demás pasos del script `run_all.sh` (mediator, facade, cliente_a, cliente_b) para que se pueda automatizar el flujo de trabajo y quede registrado en la carpeta `/logs` .

  Commits:
  - `feat(sh): (Issue #20) agregar los demas pasos del script run_all.sh` (`027442b`)
  - `docs(readme): (Issue #20) agregar documentación sobre el script run_all` (`2ec3523`)

  Pull request grupal: [#32](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/32)

## Sprint 3

- 2025-06-18: Se mejoro el script de `send_message.sh` de la carpeta `cliente_a`, el cual ahora verifica si existe la carpeta `facade/facade_dir` para guardar el mensaje, ademas toma la variable de entorno `CLIENT_A_MSG` como mensaje en el `message_a.txt`.

  Commits:
  - `feat(sh): (Issue #41) mejorar send_message.sh para que lea CLIENT_A_MSG y verifique facade_dir` (`af8dfa2`)


  Pull request grupal: [#46](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/46)

- 2025-06-19: Se mejoro el script `generar_dependencies.py` para que genere un archivo `.dot` de las dependencias reales y tener la opcion de visualizar graficamente el grafo de dependencias.

  Commits:
  - `feat(py): (Issue #43) mejorar el script generar_dependencies.py para buscar y generar .dot de dependencias` (`2dcc5ff`)
  - `feat(readme): (Issue #43) agregar documentacion de la nueva funcionalidad de generar_dependencies.py` (`98609b4`)

  Pull request grupal: [#49](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/49)

- 2025-06-19: Se actualizo los pasos que se realizo en el sprint 2 para que funcionaran (ya que dependen de otros pasos), ademas se agrego el paso `--step all` que ejecuta todo el proyecto y un paso adicional extra (`--set diagram`) que genera la imagen en PNG del diagrama de dependencias.

  Commits:
  - `feat(sh): (Issue #42) se agrego el paso --all y el paso --diagram` (`4225b7a`)

  Pull request grupal: [#51](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4/pull/51)