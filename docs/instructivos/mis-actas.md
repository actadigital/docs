# Instructivo para la aplicación web Mis Actas

## Acceso e inicio de sesión

Puede acceder a la aplicación web de control de actas haciendo [clic aquí](https://control.actadigital.com.ar/).

La aplicación **Mis Actas** solicitará que ingresemos usuario y contraseña.
Las _Entidades de control_ son las encargadas de gestionar y distribuir las credenciales de acceso.

!!! info "Credenciales de acceso"
	El usuario y contraseña para ingresar a la aplicación web es el mismo que el utilizado en la aplicación móvil.

Cuando ingresamos al sistema, vemos a la izquierda el menú principal, en la esquina superior derecha información del usuario, y en el centro de la pantalla el listado de actas.

## Mis Actas

El listado de Mis Actas muestra las 10 actas más recientemente generadas y **enviadas** por el profesional. Podemos ir cargando de a 5 actas con el botón **MOSTRAR MÁS**, o podemos cargar todas presionando **MOSTRAR TODAS**.

Las actas en estado Pendiente sólo son visibles desde la aplicación móvil.

Para cada acta del listado podemos ver:

- Su fecha de generación.
- La precisión de las coordenadas del acta.
- La distancia del acta a la parcela; parcela asociada al número de PII.
- Estado del [control de la ubicación](#control-de-ubicacion).
- Los botones de acciones.

!!! info "Control de ubicación"
    En caso de no visualizar el control de ubicación, o tener dudas respecto a este dato, consultar la sección [Control de ubicación](#control-de-ubicacion)

Las acciones que podemos realizar sobre un acta son las siguientes, en el mismo orden que la imagen:

![Acciones Mis Actas](/es/latest/img/acciones-mis-actas.png)

- Ver el [detalle](#detalle-de-un-acta).
- Acceder a la [edición](#editar-un-acta).
- Enviar el PDF del acta al mail.
- Ejecutar el [control de la ubicación](#control-de-ubicacion).

## Detalle de un acta

Desde esta pantalla, podemos ver la totalidad de los datos que contiene un acta, además de la representación visual de su ubicación, precisión de las coordenadas, y datos de control.

Para más información sobre el dato **Indicador de calidad** podemos consultar la siguiente sección: [Indicador de calidad](#indicador-de-calidad)

Si el [control de la ubicación](#control-de-ubicacion) fue realizado con éxito, en el mapa podremos ver:

- Un círculo azul centrado en la parcela. Indica el área donde se considera correcta la ubicación del acta.
- Un marcador con el icono de Acta Digital, ubicando las coordenadas del acta.
- Un círculo rojo alrededor de la ubicación del acta, indicando la precisión con la cual fueron tomadas las coordenadas.

![Mapa detalle Mis Actas](/es/latest/img/mis-actas-mapa.png)

<iframe width="560" height="315" src="https://www.youtube.com/embed/vSYZ3ppDPPw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Historial de cambios

Debajo de los detalles del acta podemos ver el listado de cambios que se han hecho sobre la misma. Vemos la fecha, el usuario que lo realizó, y los datos anteriores que tenía el acta, previos a su edición.

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

El control de ubicación (o control de calidad), es un proceso automático que realiza el sistema para determinar si la **ubicación** del acta es **correcta**, o debe revisarse. Se requieren los siguientes datos:

- dimensión y ubicación de la parcela asociada al número de PII.
- coordenadas del acta. 

El **criterio automático de control** es el siguiente: dado el encuadre de la parcela, tomamos su lado más largo L, y, con centro en el centroide de la parcela, trazamos una circunferencia de radio 2L. Por último el sistema verifica si las coordenadas del acta están dentro de dicha circunferencia o no.

Visualmente se utilizan los siguientes iconos y colores para representar el resultado del control de ubicación: 
Correcta: ![Correcta](/es/latest/img/icono-correcto.png) Revisar: ![Revisar](/es/latest/img/icono-revisar.png)

**Correcta** significa que el acta se encuentra efectivamente en las cercanías de la parcela referenciada por el número de partida.

**Revisar** siginifica que la _Entidad de control_ debe realizar un chequeo manual de la ubicación del acta, siendo la _Entidad de control_ quien determine si es Correcta o Incorrecta dicha ubicación.

### Indicador de calidad

El indicador de calidad es un número adimensional que **representa la situación de la ubicación** del acta respecto a la parcela referenciada. Es el cociente entre:

- distancia del acta al centro de la parcela
- y el radio de la circunferencia descripta en [control de la ubicación](#control-de-ubicacion).

La siguiente imagen representa estos dos datos:

![Indicador de calidad](/es/latest/img/acta_indicador_calidad.png)

La **lectura** que podemos hacer del indicador de calidad es la siguiente: 

- un valor **entre 0 y 1** indica que el acta está ubicada dentro de la circunferencia donde **se considera correcta**, por lo tanto el acta está ubicada en las cercanías de la parcela.
- un valor **mayor que 1** indica que el acta está fuera de dicha circunferencia, por lo tanto **debe realizarse una revisión manual** de la situación.

## Acta Presentada/aceptada

Un acta puede estar o no Presentada. Que un acta esté Presentada siginifica que la _Entidad de control_ ha relacionado dicho acta con un **acto** (p. ej. un acto de levantamiento parcelario). Un acta Presentada no puede asociarse con otro acto y **ya no puede ser editada**. El acta queda archivada.

Muchas actas pueden no estar presentadas/aceptadas debido a que este atributo fue implementado de forma posterior al inicio del funcionamiento del sistema.