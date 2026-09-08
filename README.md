Sistema de Turnos para Atención Estudiantil

 1. Nombre de la aplicación

Sistema de Turnos para Atención Estudiantil.

2. Descripción no técnica del problema

En una institución educativa pueden llegar varios estudiantes al mismo tiempo para realizar diferentes trámites.

Cuando esto sucede, es necesario establecer un orden de atención para evitar confusiones.

La aplicación representa una fila de estudiantes. Cada persona que llega obtiene un turno y se ubica al final de la fila. Cuando llega el momento de atender, se atiende primero a la persona que lleva más tiempo esperando.

De esta manera, el sistema organiza los turnos respetando el orden de llegada.

 3. Descripción de la solución

La aplicación fue desarrollada en Python y permite administrar una fila de estudiantes utilizando una cola implementada mediante un vector.

El programa permite:

- Agregar estudiantes.
- Mostrar los estudiantes en espera.
- Consultar el siguiente estudiante.
- Atender al primer estudiante de la fila.
- Detectar cuando la cola está llena.
- Detectar cuando la cola está vacía.

Los datos almacenados para cada estudiante son:

- Número de turno.
- Nombre.
- Motivo de la atención.

4. Estructura de datos seleccionada

La estructura seleccionada es una cola implementada mediante un vector.

La cola funciona bajo el principio FIFO, que significa "primero en entrar, primero en salir".

El vector tiene una capacidad definida y utiliza posiciones para almacenar los estudiantes.

El programa utiliza dos índices principales:

- `frente`: indica la posición del estudiante que será atendido.
- `final`: indica la siguiente posición disponible para agregar un estudiante.

 5. Justificación técnica de la elección

La cola es adecuada para este problema porque representa directamente el comportamiento de una fila de atención.

Las principales operaciones implementadas son:

 Encolar

Agrega un estudiante al final de la cola.

Desencolar

Retira y atiende al estudiante ubicado en el frente.

Consultar frente

Permite conocer quién será atendido a continuación sin retirarlo.

 Verificar si está vacía

Permite controlar el caso en el que no existen estudiantes esperando.

 Verificar si está llena

Permite controlar el límite de capacidad del vector.

La principal ventaja es que mantiene el orden de llegada.

Una de sus limitaciones es que la capacidad del vector es fija.

 6. Análisis de otra estructura

Otra estructura que podría utilizarse para resolver el mismo problema es un vector o arreglo simple.

El vector permitiría almacenar los estudiantes y acceder directamente a cada posición mediante un índice.

Sin embargo, el vector por sí solo no establece el comportamiento FIFO de una cola.

El programador tendría que controlar manualmente el orden de atención.

Además, si se elimina un estudiante de la primera posición y se desea mantener los elementos consecutivos, sería necesario desplazar los elementos restantes.

Por ejemplo, si tenemos Ana, Carlos y Laura y retiramos a Ana, habría que reorganizar las posiciones para mantener los estudiantes consecutivos.

Por esta razón, aunque un vector puede almacenar los datos, la cola resulta más adecuada para representar una fila de atención.

7. Instrucciones para ejecutar el programa

Se necesita tener instalado Python 3.

Para ejecutar el programa:

1. Descargar o clonar este repositorio.
2. Abrir una terminal en la carpeta del proyecto.
3. Ejecutar:

```bash
python sistema_turnos.py
