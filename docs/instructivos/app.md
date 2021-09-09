# Instructivo de la aplicación Acta Digital

## Introducción

La aplicación Acta Digital se ejecuta sobre un celular, y es la encargada de generar actas digitales sobre determinados actos. Un acta digital se conforma principalmente por:

- Identidad de la persona responsable
- Ubicación geográfica
- Fecha y hora

Para utilizar la aplicación se necesita un usuario y una contraseña, de modo que las acciones son registradas bajo el nombre y responsabilidad de la persona asociada a dicho usuario.

En los siguientes apartados se describen las principales funcionalidades y se detallan las instrucciones de uso.

## Inicio de sesión

Cuando abrimos la aplicación por primera vez, debemos iniciar sesión con usuario y contraseña. En los sucesivos ingresos, este paso no será necesario. 
Las _Entidades de control_ son las encargadas de gestionar y distribuir las credenciales de acceso. 

!!! info "Credenciales de acceso"
	El usuario y contraseña para la aplicación móvil es el mismo que para la aplicación web [Mis Actas](/instructivos/mis-actas).

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

Antes de guardar un acta debemos observar:

- Que la aplicación esté tomando **coordenadas**.
- Que la **precisión** tenga un valor aceptable, acorde a un navegador GPS.
- Que hayan transcurrido al menos **3 minutos** de toma de coordendas, con el fin de estabilizar coordenadas y precisión.

!!! info "Importante"
    La coordenadas guardadas son aquellaa que se obtienen al momento de presionar Guardar Acta. Por lo tanto es importante **guardar** el Acta _en las cercanías_ del lugar del acto.

### Guardar acta - Celular en comodato - Lector embebido

Si los datos ingresados son válidos, al presionar **Guardar Acta**, la aplicación solicita el ingreso de la huella digital en el sensor de huellas del celular.

![Solicitud de Huella Dactilar](/img/acta_solicitud-huella.png)

Con sólo tocar el sensor de huellas es suficiente. Una vez reconocida la huella, el Acta se guarda y es posible visualizarla en el [listado de actas](#pantalla-de-inicio).

### Guardar acta - Token biométrico USB

Si los datos ingresados son válidos, al presionar **Guardar Acta**, la aplicación solicita que conectemos nuestro Token biométrico USB. Mientras tanto vemos el mensaje _Esperando hardware_. 

Una vez conectado el token, la aplicación solicita el ingreso de alguna huella digital. Presionamos el sensor del token y el acta se guarda.

## Detalles de un acta

Si seleccionamos una fila del listado de actas, podemos acceder a los detalles del acta seleccionada.

Desde esta pantalla se puede acceder a la [edición de un acta](#editar-un-acta), o podemos anular o quitar anulación de las mimas.

![Detalle de un Acta](/img/acta_detalle.png)

Además podemos ver, en caso de contar con conexión a Internet, las coordenadas del acta sobre un mapa de Google Maps.

## Enviar actas

El envío de actas se realiza desde el [listado](#pantalla-de-inicio) de las mismas. 
Podemos **enviar todas** las actas pendientes usando la opción _Enviar actas_ del menú. También podemos mantener apretado un acta y **seleccionar** cual o cuáles queremos enviar.

!!! info "Importante"
	Para realizar el envío de actas es necesario que el celular este conectado a **internet**.

Una vez enviadas las actas, estas estarán disponibles para administrar a través de [Mis Actas](/instructivos/mis-actas) y serán visibles para las _Entidades de control_.

![Enviar todas la Actas Pendientes](/img/acta_enviar-todas.png)

*Presionando __Enviar Actas__, serán enviadas todas las actas en Estado Pendiente.*

![Seleccionar Actas para enviar](/img/acta_enviar.png)

*Aquí pueden verse seleccionadas las actas número 2 y 3.*

## Editar un acta

Pueden editarse aquellas actas en estado **Pendiente**. La fecha y la ubicación geográfica no pueden ser modificadas, ni tampoco la aplicación las modifica.

Para guardar los cambios se solicitará ingresar nuevamente la huella digital.

## Mostrar sólo pendientes

Acción de la [pantalla de inicio](#pantalla-de-inicio) que permite ocultar del listado aquellas actas que estén enviadas o anuladas.

## Copia de seguridad

Esta opción, accesible desde la [pantalla de inicio](#pantalla-de-inicio), permite realizar una copia de seguridad de las actas pendientes. Las actas pendientes se guardan en la nube, por lo tanto es necesario que el celular esté conectado a internet. 

!!! info "Copia de seguridad automática"
	La aplicación realiza copias de seguridad automáticamente. Con la opción _Copia de seguridad_ podemos realizarla a demanda, en casos que consideremos necesarios; por ejemplo, hemos realizado varias actas, tenemos que seguir trabajando y queremos resguardar las actas ya hechas, o vamos a cambiar de celular y tenemos actas pendientes.

## Profesional asociado

En esta opción accesible desde la pantalla de inicio, podemos ver los datos del profesional que inició sesión. 

## Sincronizar actas

Opción que permite descargar y guardar en el celular todas las actas que hayamos hecho y estén en el sistema. También recupera las actas en estado Pendiente que hayan sido respaldadas en las copias de seguridad.

La opción de sincronizar actas es útil en casos de cambio de celular o reinstalación de la aplicación.

## Reinstalación de la aplicación

Podemos requerir reinstalar la aplicación en casos de cambio de celular, o fallas en el mismo. Para evitar perder datos debemos realizar los siguientes pasos:

- De ser posible, realizar [copia de seguridad](#copia-de-seguridad) en el celular actualmente en uso.
- Instalar la aplicación, ya sea en otro celular o nuevamente en el mismo. La podemos encontrar en la tienda oficial.
- [Iniciar sesión](#inicio-de-sesion)
- Ingresar en la opción [Sincronizar actas](#sincronizar-actas)
