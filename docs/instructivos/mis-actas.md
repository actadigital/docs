# Instructivo para la aplicación web Mis Actas

## Acceso e inicio de sesión

Para acceder a la aplicación web debemos ingresar al [sitio web de Acta Digital](https://actadigital.com.ar/), ingresar en la opción USUARIOS y luego presionar el botón MIS ACTAS.

La aplicación **Mis Actas** solicitará que ingresemos usuario y contraseña.
Las _Entidades de control_ son las encargadas de gestionar y distribuir las credenciales de acceso.

!!! info "Credenciales de acceso"
	El usuario y contraseña para ingresar a la aplicación web es el mismo que el utilizado en la aplicación móvil.

Cuando ingresamos al sistema, vemos a la izquierda el menú principal, en la esquina superior derecha información del usuario, y en el centro de la pantalla el listado de actas.

## Mis Actas

El listado de Mis Actas muestra inicialmente las 10 actas más recientemente generadas y **enviadas** por el profesional. Podemos ir cargando de a 5 actas con el botón **MOSTRAR MÁS**, o podemos cargar todas presionando **MOSTRAR TODAS**.

Las actas pendientes sólo son accesibles desde la aplicación móvil.

Para cada acta podemos ver:

- Su fecha de generación.
- La precisión del sensor GPS al momento de tomar las coordenadas.
- La distancia del acta a la parcela; parcela asociada al número de PII.
- Estado del [control de la ubicación](#control-de-ubicacion).
- Los botones de acciones.

!!! info "Control de ubicación"
    En caso de no visualizar el control de ubicación, o tener dudas respecto a este dato, consultar la sección [Control de ubicación](#control-de-ubicacion)

Las acciones que podemos realizar sobre un acta son las siguientes, en el mismo orden que la imagen:

![Acciones Mis Actas](/img/acciones-mis-actas.png)

- Ver el [detalle](#detalle-de-un-acta).
- Acceder a la [edición](#editar-un-acta).
- Enviar el PDF del acta al mail.
- Ejecutar el [control de la ubicación](#control-de-ubicacion).

## Detalle de un acta

Desde esta pantalla, podemos ver la totalidad de los datos que contiene un acta, además de la representación visual de su ubicación, precisión de las coordenadas, y datos de control.

De los datos mostrados, es importante explicar el dato Indicador de calidad, desarrollado en la siguiente seccion: [Indicador de calidad](#indicador-de-calidad)

Si el control de la ubicación fue realizado con éxito, en el mapa podremos ver:

- Un círculo azul con centro en la parcela referida en el acta. El círculo indica el área donde se considera correcta la ubicación del acta.
- Un marcador con el icono de Acta Digital, indicando las coordenadas del acta.
- Un círculo rojo alrededor de la ubicación del acta, indicando la precisión con la cual fueron tomadas las coordenadas.

![Mapa detalle Mis Actas](/img/mis-actas-mapa.png)

<iframe width="560" height="315" src="https://www.youtube.com/embed/vSYZ3ppDPPw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Historial de cambios

## Editar un acta

Las actas que observamos en el listado de Mis Actas se encuentran en estado **Enviado**. Sin embargo, podemos editar ciertos datos:

- Número de Partida de Impuesto Inmobiliario.
- Comitente.
- Ocupante y calidad de ocupación.
- Observaciones.

Editar un acta desde esta aplicación no implica alterar su fecha ni coordenadas.

La modificación del número de partida conlleva a una nueva ejecución del [control de la ubicación](#control-de-ubicacion). La aplicación **automáticamente** dispara este control.

<iframe width="560" height="315" src="https://www.youtube.com/embed/VhqQZKresVg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Control de ubicación

El control de ubicación (o control de calidad), es el proceso mediante el cual el sistema busca determinar si la ubicación del acta es correcta, o debe revisarse. Se utilizan los datos de la localización del acta, y las dimensiones y ubicación de la parcela asociada al número de PII. 

El **criterio de control** es el siguiente: dado el encuadra de la parcela, tomamos su lado más largo L, y con centro en el centroide de la parcela trazamos una circunferencia de de radio 2L. Por último el sistema verifica si las coordenadas del acta están dentro de dicha circunferencia o no.

Correcta: ![Correcta](/img/icono-correcto.png) Revisar: ![Revisar](/img/icono-revisar.png)

### Indicador de calidad