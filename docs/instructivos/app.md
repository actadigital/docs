# Instructivo de la aplicación Acta Digital

## Introducción 

La aplicación Acta Digital se ejecuta sobre un celular, y es la encargada de generar actas digitales. 

Para utilizar la aplicación es necesario acceder con usuario y contraseña, de modo que las acciones son registradas bajo el nombre y responsabilidad de la persona asociada a dicho usuario.

En los siguientes apartados se describen las principales funcionalidades y se detallan las instrucciones de uso.

## Inicio de sesión

Cuando abrimos la aplicación por primera vez, debemos iniciar sesión con usuario y contraseña. En los sucesivos ingresos, este paso no será necesario. 
Las _Entidades de control_ son las encargadas de gestionar y distribuir las credenciales de acceso. 

!!! info "Credenciales de acceso"
	El usuario y contraseña para la aplicación móvil es el mismo que para la aplicación web [Mis Actas](mis-actas.md).

## Pantalla de inicio

Podemos observar el listado de actas realizadas. Inicialmente se encuentra vacío. Cada ítem del listado muestra el número identificador del acta, el icono que representa su estado, y algún dato adicional. Presionando sobre un acta podemos ver los [detalles](#detalles-de-un-acta) de la misma.

![Listado de Actas](/es/latest/img/acta_lista.png)

En la parte superior derecha podemos ver las acciones disponibles, mientras que en la esquina inferior derecha vemos el botón **+**, para generar un nuevo acta.
En las siguientes secciones se detalla la funcionalidad de cada acción.

## Generación de un nuevo acta

La generación de un nuevo acta se accede desde el listado de actas, con el botón **+** ubicado en la parte
inferior derecha. Al presionarlo se abre la siguiente pantalla:

![Nueva Acta](/es/latest/img/acta_nuevo.png)

Los **pasos a seguir** son:

- Completar los datos del acta
- Controlar los datos de ubicación
- Guardar

### Completar los datos del acta

- **Partida de Impuesto Inmobiliario** _(obligatorio)_: Se ingresan sólo números, la aplicación le da el formato apropiado y calcula el dígito de control.
- **Comitente** _(obligatorio)_: Nombre y apellido del comitente.
- **Ocupante** _(obligatorio)_: Nombre y apellido del ocupante, si lo hay.
- **Calidad de ocupación**: Seleccionar una de las opciones. En caso de no corresponder ninguna, podrá seleccionar _Otro_ y detallar en _Nota u observación_.
- **Nota u observación**: Aclaración que crea pertinente.

La **ubicación geográfica** (latitud y longitud) es obtenida **automáticamente**. Mientras la aplicación resuelve la ubicación veremos la leyenda _Buscando coordenadas_ y **no podremos guardar el acta**. Debemos esperar a que el celular tome coordenadas.

!!! info "El GPS debe funcionar sin Internet"
    La obtención de coordenadas **debe funcionar** con GPS, sin necesidad de acceso a Internet. De todos modos, la conexión a Internet agiliza y acelera este proceso. 
	Consultar las siguientes [recomendaciones](../recomendaciones.md).

### Controlar los datos de ubicación

La aplicación nos proporciona información para que sepamos en qué estado se encuentra el proceso de toma de coordenadas. En la imagen de Nuevo Acta, podemos ver:

- **Tiempo transcurrido**: Indica el tiempo transcurrido desde el inicio de la toma de coordeandas.
- **Satélites**: Muestra el número de satélites que están siendo utilizados para fijar las coordenadas. Si, por ejemplo, vemos **0/10**, significa que se están utilizando 0 satélites de 10 visibles, y no estamos obteniendo coordenadas del sistema GPS. Debemos buscar un sitio más despejado. Si por ejemplo vemos **1/10**, o 2, es posible que tengamos mal la fecha y hora del celular, no pudiendo establecer comunicación con los satélites. Un **caso normal de funcionamiento** es ver 4/12, 10/20.
- **Precisión**: De las coordeandas. Mejora con el paso de los minutos. Utilizando sólo sistema GPS podremos ver 4 o 6 metros. Asistiendo al GPS con Internet la precisión suele empeorar, siendo típicamente 20 u 80 metros.
- **Coordenadas**: Se intentan obtener cada 5 o 10 segundos. Se van ajustando con el pasar de los minutos.

**Antes de guardar un acta debemos controlar**:

- Que la aplicación haya tomando **coordenadas**.
- Que la **precisión** tenga un valor aceptable, acorde a un navegador GPS.
- Que hayan transcurrido al menos **3 minutos desde la obtención de la primera coordenada**, con el fin de estabilizar las coordenadas y la precisión.

!!! info "Importante"
    La coordenadas guardadas son aquellaa que se obtienen al momento de presionar Guardar Acta. Por lo tanto es importante **guardar** el Acta _en las cercanías_ del lugar del acto.

### Guardar acta - Celular en comodato - Lector embebido

Si los datos ingresados son válidos, al presionar **Guardar Acta**, la aplicación solicita el ingreso de la huella digital en el sensor de huellas del celular.

![Solicitud de Huella Dactilar](/es/latest/img/acta_solicitud-huella.png)

Con sólo tocar el sensor de huellas, es suficiente. Una vez reconocida la huella, el Acta se guarda y es posible visualizarla en el [listado de actas](#pantalla-de-inicio).

### Guardar acta - Token biométrico USB

Si los datos ingresados son válidos, al presionar **Guardar Acta**, la aplicación solicita que conectemos nuestro Token biométrico USB. Mientras tanto veremos el mensaje _Esperando hardware_. 

Una vez conectado el token, la aplicación solicita el ingreso de alguna huella digital. Presionamos el sensor del token y el acta se guarda.

## Detalles de un acta

Si seleccionamos una fila del listado de actas, podemos acceder a los detalles del acta seleccionada.

Desde esta pantalla se puede acceder a la [edición de un acta](#editar-un-acta), o podemos anular o quitar la anulación de la misma.

![Detalle de un Acta](/es/latest/img/acta_detalle.png)

Además podemos ver, en caso de contar con conexión a Internet, las coordenadas del acta sobre un mapa de Google Maps.

## Enviar actas

El envío de actas se realiza desde el [listado de actas](#pantalla-de-inicio). 
Podemos elegir **enviar todas** aquellas actas en estado _Pendiente_ presionando el botón _Enviar actas_. También podemos mantener presionado sobre un acta del listado y **seleccionar** cual o cuáles deseamos enviar.

!!! info "Importante"
	Para realizar el envío de actas es necesario que el celular este conectado a **Internet**.

Una vez enviadas las actas, éstas estarán disponibles para administrar a través de [Mis Actas](mis-actas.md), y serán visibles para las _Entidades de control_.

![Enviar todas la Actas Pendientes](/es/latest/img/acta_enviar-todas.png)

*Presionando __Enviar Actas__, serán enviadas todas las actas en estado Pendiente.*

![Seleccionar Actas para enviar](/es/latest/img/acta_enviar.png)

*Aquí pueden verse seleccionadas las actas número 2 y 3.*

## Editar un acta

Desde la aplicación móvil pueden editarse sólo aquellas actas en estado **Pendiente**. La fecha y la ubicación geográfica no pueden ser modificadas, ni tampoco la aplicación las modifica.

Para guardar los cambios se solicitará ingresar nuevamente la huella digital.

## Mostrar sólo pendientes

Acción de la [pantalla de inicio](#pantalla-de-inicio) que permite ocultar del listado aquellas actas que estén enviadas o anuladas.

## Copia de seguridad

Esta opción, accesible desde la [pantalla de inicio](#pantalla-de-inicio), permite realizar una copia de seguridad de las actas pendientes. Las actas pendientes se guardan en la nube, por lo tanto es necesario que el celular esté conectado a Internet. 

!!! info "Copia de seguridad automática"
	La aplicación realiza copias de seguridad automáticamente. Con la opción _Copia de seguridad_ podemos realizarla a demanda, en casos que consideremos necesarios; por ejemplo, hemos realizado varias actas, tenemos que seguir trabajando y queremos resguardar las actas ya hechas, o vamos a cambiar de celular y tenemos actas pendientes.
	
![Copia de seguridad](/es/latest/img/acta_backup.png)

## Profesional asociado

En esta opción, accesible desde la pantalla de inicio, podemos ver los datos del responsable de las actas realizadas. 

### Actualizar datos del usuario

Dentro de la pantalla de Profesional asociado, si presionamos los 3 puntitos de arriba a la derecha, encontraremos el botón Actualizar datos.
![Actualizar datos del usuario](/es/latest/img/actualizar_datos.png)
Presionando este botón, la aplicación vuelve a descargar los datos el usuario. Previamente se debe solicitar al equipo de soporte que modifique los datos. También el equipo de soporte puede solicitar eventualmente que presione este botón. 

## Sincronizar actas

Opción que permite descargar y guardar en el celular todas las actas que hayamos hecho y estén en el sistema. También recupera las actas en estado Pendiente que hayan sido respaldadas en las copias de seguridad.

La opción de sincronizar actas es útil en casos de cambio de celular o reinstalación de la aplicación.

## Reinstalación de la aplicación

Podemos requerir reinstalar la aplicación en casos de cambio de celular, o falla del mismo. Para evitar perder datos, debemos realizar los siguientes pasos:

- De ser posible, realizar la [copia de seguridad](#copia-de-seguridad) en el celular actualmente en uso.
- Instalar la aplicación, ya sea en otro celular o nuevamente en el mismo. La podemos encontrar [aquí](https://actadigital.com.ar/#download).
- [Iniciar sesión](#inicio-de-sesion).
- Ingresar en la opción [Sincronizar actas](#sincronizar-actas) para descargar nuestras actas al celular.
