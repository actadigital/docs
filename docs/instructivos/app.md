# Instructivo de la aplicación **Acta Digital**

## Introducción
La aplicación Acta Digital se ejecuta sobre un celular, y es la encargada de generar actas digitales sobre determinados actos. Un acta digital se conforma principalmente por:

- Identidad de la persona responsable
- Ubicación geográfica
- Fecha y hora

Para utilizar la aplicación se necesita un usuario y una contraseña, de modo que las acciones son registradas bajo el nombre y responsabilidad de la persona asociada a dicho usuario.

En los siguientes apartados se describen las principales funcionalidades y se detallan las instrucciones de uso.

## Inicio de sesión
Cuando abrimos la aplicación por primera vez, debemos iniciar sesión con usuario y contraseña. En los sucesivos ingresos, este paso no será necesario. 
Las _Entidades de control_ son las encargadas de gestionar y distribuir las credenciales de acceso a la aplicación y al sistema Acta Digital.

## Pantalla de inicio
Podemos observar el listado de actas realizadas. Inicialmente se encuentra vacío. Cada ítem del listado muestra el número identificador del acta, el icono que representa su estado, y algún dato adicional. Presionando sobre un acta podemos ver los [detalles](#detalles-de-un-acta) de la misma.

![Listado de Actas](/img/acta_listado.png)

En la parte superior derecha podemos ver las acciones disponibles, mientras que en la esquina inferior derecha vemos el botón **+**, para generar un nuevo acta.
En las siguientes secciones se detalla la funcionalidad de cada acción.

## Generación de un nuevo acta
La generación de un nuevo acta se accede desde la pantalla de inicio (listado de actas), con el botón **+** ubicado en la parte
inferior derecha. Al presionarlo se abre la siguiente pantalla:

![Nueva Acta](/img/acta_nueva.png)

Los pasos a seguir son:

- Completar datos del acta
- Controlar datos de ubicación
- Guardar

### Completar datos del acta
- **Partida de Impuesto Inmobiliario** _(obligatorio)_: Número completo de PII. A medida que se ingresan los números, la aplicación va dando el formato apropiado y calcula el dígito de control de API. El dígito de control se muestra a la derecha del número de PII y no debe ingresarse. Se recomienda verificar que sea correcto.

- **Comitente** _(obligatorio)_: Nombre y apellido del comitente.
- **Ocupante** _(obligatorio)_: Nombre y apellido del ocupante, si lo hay.
- **Calidad de ocupación**: Seleccionar una de las opciones. En caso de no corresponder ninguna, podrá seleccionar _Otro_ y detallar en _Nota u observación_.
- **Nota u observación**: Cualquier aclaración que crea pertinente.

La **ubicación geográfica** (latitud y longitud) es obtenida automáticamente. Mientras la aplicación resuelve la ubicación veremos la leyenda _Buscando coordenadas_
Hasta tanto no haya coordenadas, no podremos guardar el acta, por lo que debemos esperar.

!!! info "Importante"
    La aplicación solicita al receptor GPS coordenadas cada 10 segundos. Es importante no obstaculizar la visibilidad de satélites GPS del dispositivo (techos, árboles, edificios, etc.). Por favor, lea [estas recomendaciones](/preguntas-frecuentes/recomendaciones/) para hacer un uso óptimo de la aplicación. 

### Controlar datos de ubicación
Antes de guardar un acta debemos controlar que la aplicación nos muestre coordenadas, que la **precisión** sea acorde a la de un navegador GPS y que hayan transcurrido al menos **3 minutos** de toma de coordendas.

!!! info "Importante"
    Recordar que la ubaición guardada es aquella que se obtiene al momento de presionar Guardar Acta. Con lo cual, es importante **guardar** el Acta _en las cercanías_ del lugar del acto.

### Guardar acta - Lector embebido
Si los datos ingresados son válidos, al presionar **Guardar Acta**, la aplicación solicita el ingreso de la huella digital en el sensor de huellas del celular.

![Solicitud de Huella Dactilar](/img/acta_solicitud-huella.png)

Con sólo tocar el sensor de huellas es suficiente. Una vez reconocida la huella, el Acta se guarda y es posible visualizarla en el [listado de actas](#pantalla-de-inicio).

### Guardar acta - Token biométrico USB
Si los datos ingresados son válidos, al presionar **Guardar Acta**, la aplicación solicita que conectemos nuestro Token biométrico USB. Mientras tanto vemos el mensaje _Esperando hardware_. Una vez conectado el token, la aplicación solicita el ingreso de alguna huella digital. Presionamos el sensor y el acta se guarda.

## Detalles de un acta
Desde esta pantalla se puede acceder a la [edición de un acta](#editar-un-acta) y anular o quitar anulación de las mimas.

![Detalle de un Acta](/img/acta_detalle.png)

Además, podemos ver, en caso de contar con conexión a Internet, las coordenadas del acta sobre un mapa de Google Maps.

## Envío de Actas
El envío de actas se realiza desde el [listado](#pantalla-de-inicio) de las mismas. 
Podemos **enviar todas** las actas pendientes usando la opción _Enviar actas_ del menú. También podemos mantener apretado un acta y **seleccionar** cual o cuáles queremos enviar.

!!! info "Importante"
	Para realizar el envío de actas es necesario que el celular este conectado a **internet**.

Una vez enviadas las actas, estas estarán disponibles para administrar a través de [Mis Actas](#) y serán visibles para las _Entidades de control_.

![Enviar todas la Actas Pendientes](/img/acta_enviar-todas.png)

*Presionando __Enviar Actas__, serán enviadas todas las actas en Estado Pendiente.*

![Seleccionar Actas para enviar](/img/acta_enviar.png)

*Aquí pueden verse seleccionadas las actas número 2 y 3.*

## Editar un acta
Pueden editarse sólo aquellas actas en estado **Pendiente**. La fecha del acta y la ubicación geográfica no pueden ser modificadas, ni tampoco la aplicación las modifica.

Para guardar los cambios la aplicación solicitará ingresar nuevamente la huella digital.

## Mostrar sólo pendientes
Acción de la [pantalla de inicio](#pantalla-de-inicio) que permite ocultar del listado de actas aquellas que estén enviadas o anuladas.

## Copia de seguridad
Acción de la [pantalla de inicio](#pantalla-de-inicio) que realiza una copia de seguridad de aquellas actas pendientes. Esto permite..

## Profesional asociado

## Sincronizar actas
