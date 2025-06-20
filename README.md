# Gestion de dependencias en IaC con patrones Facade Adapter y Mediator

# Información Personal

- **Nombre completo:** Jharvy Jonas Cadillo Tarazona
- **Código:** 20210184E  
- **Correo institucional:** jharvy.cadillo.t@uni.pe

# Proyecto del Grupo 8

- **Título del proyecto:** Gestion de dependencias en IaC con patrones Facade Adapter y Mediator (Proyecto 4)
- **Repositorio grupal:** [https://github.com/Jharvichu/PC3_Grupo8_Proyecto4](https://github.com/Jharvichu/PC3_Grupo8_Proyecto4)

## Mi Rol en el Equipo
Durante el primer sprint, realicé el test de `adapter_output.py` del modulo **adapter**. En el último sprint, actualice el script `send_message.sh` del **cliente a**. Además, contribuí en los scripts principales como `run_all.sh` y la generacion, visualización de dependencias con el script `generar_dependencias.py`. Mi trabajo se centró en la validación de salidas, comunicación entre módulos y automatización de ejecuciones.

## Instrucciones para Clonar y Reproducir Mi Parte del Código

1. **Clona el repositorio grupal:**
   ```bash
   git clone https://github.com/Jharvichu/PC3_Grupo8_Proyecto4.git
   cd PC3_Grupo8_Proyecto4
   ```

2. **Ejecutamos el setup: (en el proyecto completo)**
   ```bash
   # En la raiz del repositorio
   source setup.sh
   ```

3. **Ejecutamos la parte avanzada de mi codigo en el proyecto:**

    Como mi parte avanzada con `run_all.sh` ejecua todo los módulos, para ver su funcionamiento debemos ejecutar los pasos que se tienen:

   1. Ejecutar el modulo adapter
        ```bash
        source scripts/run_all.sh --step adapter
        ```
   2. Ejecutar el modulo facade
        ```bash
        source scripts/run_all.sh --step facade
        ```
   3. Ejecutar el modulo mediator
        ```bash
        source scripts/run_all.sh --step mediator
        ```
   4. Ejecutar el cliente A
        ```bash
        source scripts/run_all.sh --step cliente_a
        ```
   5. Ejecutar el cliente B
        ```bash
        source scripts/run_all.sh --step cliente_b
        ```    
   6. Ejecutar el diagrama de dependencias
        ```bash
        source scripts/run_all.sh --step diagram
        ```   
    7. Ejecutar todo el proyecto
        ```bash
        source scripts/run_all.sh --step all
        ```  

    Para ejecutar la generación de dependencias del proyecto, se escribe el siguiente comando:

    ```bash
    python3 generar_dependencies.py
    dot -Tpng dependencies.dot -o dependencies.png
    ```
    
    Obtenemos un archivo `dependencies.json`, `dependencies.dot` y la imagen del grafo `dependencies.png`

4. **Notas adicionales:**
   - Si se ejecutan estos escripts por si solos, no deberian funcionar, ya que estos dependen que los modulos existan para que funcione.

---
