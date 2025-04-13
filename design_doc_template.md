# Titulo: Template de documento de diseño

---
El título debe ser descriptivo y reflejar claramente el enfoque del documento. En este ejemplo, se utiliza "Camera Reviews" como título, lo que inmediatamente indica el tema central. Asegúrate de que el título resuene con el contenido y objetivo del proyecto.

## Overview: Problema a resolver
Descripción..

Puedes copiar y pegar la definición del problema proporcionada por el cliente, asegurándote de incluir los detalles esenciales que guiarán el desarrollo

Ej:
La empresa "RandomCameraReviews" necesita un sistema que permita que fotografos profesionales suban "reviews" de Camaras fotograficas, para que cualquier persona desde cualquier parte del mundo pueda buscar los los reviews y comprarlas a travez de su portal. La empresa cuenta con un equipo de developers especializado en frontEnd que realizara un portal para que los editores suban los "reviews" y los usuarios puedan verlos, y han solicitado que tu como especista en Backend, les proporciones un sistema, incluyendo API que permita realizar lo siguiente:

Subir reviews de Camaras fotograficas
Obtener el contenido de los reviews para mostrarlo en vistas del portal en sus versiones web y mobile.
Manejo de usuarios para editores (no incluye visitantes que leen los reviews)
Tambien se sabe que la empresa "RandomCameraReviews" planea distribuir mayormente en America del Sur donde esta su mercado mas grande, pero tambien tienen ventas en norte america, Europa, y muy pocas en Asia.


### Alcance(Scope)
Descripción..

crucial para determinar las capacidades del sistema y las limitaciones. Estos elementos no solo guían el desarrollo, sino que también ayudan a gestionar las expectativas del cliente.

El alcance debe complementarse con los casos de uso, detallando lo que está dentro y fuera de sus límites. Por ejemplo, un usuario no registrado no debería poder subir una review, solo leerlas. Esta claridad es vital para evitar malentendidos durante el desarrollo.

#### Casos de uso
Descripción...
* Caso de uso 1
* Caso de uso 2
* ...

  EJ:
* Caso de uso 1: Como editor me gustaria poder subir una revision de una camara 
* Caso de uso 2: Como editor me gustaria poder subir una review de un lente para las camaras
* Caso de uso 3: Como usario me gustaria poder leer las reviews

Como editor quiero subir un review de cualquier objeto relacionado con la fotogarfia
Como lector quiero poder leer los reviews
Como lector quiero puntear reviews
Como lector quiero puntear comentar
Como lector quiero viajar a travéz de categorias
Como lector quiero buscar reviews especificas
Como administrador quiero gestionar mis editores
 
#### Out of Scope (casos de uso No Soportados)
Descripción...
* Caso de uso 1
* Caso de uso 2
* ...

 * Como usuario no registrado me gustaria poder subir una review de una camara
* Como editor me gustaria dar feedback a otras review
* Como editor me gustaria aprobar comentarios en reviews de usuario registrados
* Como usuario no registrado me gustaria registrarme
* Como usuario no registrado me gustaria poder compartir una review en mis redes sociales
* Como usuario registrado me gustaria comentar en las reviews
* Como usuario registrado me gustaria dar seguimiento de los comentarios en la reviews que me interesan
* Como usuario no registrado quiero subir un review de una camara
* Como usuario no registrado quiero puntear un review
* Como usuario no registrado quiero comentar en un review
* Como administrador quiero obtener estadisticas de los reviews
---
## Arquitectura

representación visual y teórica de cómo interactúan los diferentes elementos del sistema

siempre preguntar el porque , para hacer una revisión del diseño 

Plasmar un borrador  
¿ que servicios vamos a tener? ¿ Que comunicaciones deeben tener? 


Tomar un par de casos de usos principales
y hacer algunas preguntas 

¿cuantos usuarios? 
¿cuantos editores ? 
¿Cuales son los tiempos de respuesta para escritura (r) y para lectura (w)? 

a partir de lo anterior sabemos si debemos crear un servicios separados uno para escritura y otro para escritura, si se va a usar sistemas de cache

Te van a permitir definir mejor el sistema, si necesitar crear mejores soluciónes

### Diagramas
poner diagramas de secuencia, uml, etc

### Modelo de datos
Poner diseño de entidades, Jsons, tablas, diagramas entidad relación, etc..

---
## Limitaciones
Lista de limitaciones conocidas. Puede ser en formato de lista.
Ej.
* Llamadas del API tienen latencia X
* No se soporta mas de X llamadas por segundo
---

La llamada al API no debe exceder una latencia de 500 milisegundos al subir una review.
La latencia para obtener reviews debe ser menor a 100 milisegundos.
Estas restricciones son necesarias para asegurar la eficiencia y funcionalidad del sistema a medida que crece.

## Costo
Descripción/Análisis de costos
Ejemplo:
"Considerando N usuarios diarios, M llamadas a X servicio/baseDatos/etc"
* 1000 llamadas diarias a serverless functions. $XX.XX





------


Un ejemplo clave

# Sala de conciertos

---

## Overview: 

Se requiere visibilizar los proximos eventos de las agrupaciones musicales de forma ordenada según calendario. Estos eventos serán cargados por los mismos organizadores de los eventos o por las mismas bandas en una pantalla emergente de gestión. Una vez que cada evento se cree se generará un código único. de 8 digitos. Una vez cada evento alcance su fecha de ejecución más un día será retirado de la lista. Los eventos podrán ser eliminados de la lista con un código único generado. En caso de que haya varios eventos en la misma fecha, no se hará organización adicional.

### Alcance(Scope)

Desarrollo de un portal web de visualización libre de publicidad acorde a los eventos de agrupaciones musicales, la cual puede ser cargada, modificada y eliminada unicamente por los gestores del evento.

#### Casos de uso

Descripción...

* Como **espectador** quiero entrar a la página principal y ver un listado de los próximos eventos.
* Como **espectador** quiero ver el listado de los próximos eventos organizados por la fecha.
* Como **espectador** me gustaría al hacer clic, ver información más detallada del evento.
* Cómo **gestor** quiero ver un botón que me permita acceder a una página de gestión de eventos.
* Cómo **gestor** quiero poder ver dos opciones iniciales en la pantalla emergente de gestíon de eventos: Crear evento y Gestionar evento.
* Cómo **gestor** quiero poder crear un evento cargando el flyer de la banda y demás información asociada al mismo.
* Cómo **gestor** quiero recibir en mi celular un SMS y un correo indicando el código único de gestión del evento, una vez el evento haya sido creado.
* Cómo **gestor** estando ubicado en la pantalla de Gestionar Evento, quiero poder ingresar el código que recibí previamente.
* Cómo **gestor** al ingresar correctamente el código, quiero ver una ventana que me permita editar la información del evento o eliminarlo de ser requerido.

#### Out of Scope (casos de uso No Soportados)

Descripción...

* Como **espectador** me gustaría filtrar los eventos por fecha, ubicación, género, etc.
* Cómo **gestor** me gustaría personalizar la forma en que se visualiza mi evento.
* Cómo **gestor** me gustaría tener un botón de compra de boleteria en cada evento.
* Cómo **dueño del portal** me gustaría compartir automaticamente los eventos creados en todas mis redes sociales el día anterior y el dia del evento.
* 1000 read/write units diarias a X Database on-demand. $XX.XX
Total: $xx.xx (al mes/dia/año)
