---
title: Ejecutar una revisión de campaña en canales múltiples
description: Utilice CX Enterprise MCP en una sola sesión de IA para obtener una vista unificada del estado de las campañas de AJO, CJA y Real-Time CDP en los recorridos, las audiencias y el rendimiento.
last-substantial-update: 2026-06-09T00:00:00Z
index: false
source-git-commit: 94c7d3c6b0542b6e27d8775f78acf40a1b1cae91
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 5%

---


# Ejecutar una revisión de campaña en canales múltiples

<!-- last-modified: 2026-05-21 -->

![Ejecutar una revisión de campaña en canales múltiples](https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review)

Una imagen completa del estado de la campaña requiere datos de varios sistemas: recorridos activos de AJO, estado de activación de audiencia de Real-Time CDP y métricas de rendimiento de CJA. Este tutorial muestra cómo conectar los tres elementos en una sola sesión de IA para que pueda pasar del estado del recorrido al estado de la audiencia y las tendencias de rendimiento en una conversación en lugar de usar tres herramientas independientes.

| Detalles del escenario | |
| --- | --- |
| **Aplicaciones empresariales de CX** | [Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/ajo-home), [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), [Real-Time CDP](https://experienceleague.adobe.com/es/docs/experience-platform/rtcdp/home) |
| **Herramientas agénticas** | [MCP de CX Enterprise](../tools/mcp-servers.md#cx-enterprise-mcp-servers) |
| **Audiencia** | Administradores de campañas, operaciones de marketing |
| **Requisito previo** | Cliente de IA compatible con MCP, acceso a AJO, CJA y Real-Time CDP |

Cada paso muestra un mensaje representativo y un ejemplo de respuesta de IA. **Más cosas que puedes hacer** sección sigue para una exploración adicional en la misma sesión.

## Antes de empezar

>[!BEGINTABS]

>[!TAB Claude.ai]

Conecte CX Enterprise MCP como un conector personalizado. Una conexión le permite acceder a las herramientas de AJO, CJA y Real-Time CDP.

1. Vaya a **Configuración > Integraciones** en Claude.ai.
2. Seleccione **Agregar conector personalizado** e introduzca la dirección URL del servidor: `https://cx-enterprise.adobe.io/mcp`
3. Seleccione **Conectar** e inicie sesión con su Adobe ID.

Configuración completa: [Documentación de conectores personalizados Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Conecte el MCP de CX Enterprise mediante el modo de desarrollador de ChatGPT (se requiere plan profesional, avanzado, empresarial, empresarial o educativo).

1. Habilitar **Modo de desarrollador** en **Configuración de ChatGPT**.
2. Vaya a **Configuración > Integraciones** y seleccione **Agregar conector personalizado > Servidor MCP remoto**.
3. Escriba la dirección URL del servidor: `https://cx-enterprise.adobe.io/mcp`
4. Seleccione **Conectar** e inicie sesión con su Adobe ID.

Configuración completa: [Documentación de MCP de ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Otros clientes de IA]

¿Utiliza Gemini, Microsoft Copilot, Cursor, Claude Code u otro entorno compatible con MCP? Conéctese a CX Enterprise MCP utilizando este punto de conexión:

```
https://cx-enterprise.adobe.io/mcp
```

Instrucciones de configuración completas para todos los clientes admitidos: [Conéctese a su cliente de IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Inicie sesión con su Adobe ID cuando se le solicite y seleccione la organización de IMS vinculada a sus entornos de AJO, CJA y Real-Time CDP. La elección de una organización incorrecta es la fuente más común de errores de autenticación.
>
>En la primera conexión, el cliente de IA puede pedirle que seleccione una organización de IMS o que especifique una zona protegida. Una vez establecido ese contexto, el servidor MCP lo utiliza para el resto de la sesión.
>
>Algunas herramientas le piden su aprobación antes de ejecutarse. Revise la solicitud y apruébela o rechace. No se realiza ninguna acción sin su confirmación.

## Paso 1: Revisar los recorridos y campañas activos

Comience por AJO para establecer lo que se está ejecutando actualmente. Saber qué recorridos están activos y los modificados recientemente proporciona la base para el resto de la revisión.

```
What journeys are currently active in AJO?
```

+++Ver una respuesta de ejemplo

Se han encontrado 8 recorridos activos en su organización de AJO:

| Recorrido | Canal(s) | Última modificación |
| --- | --- | --- |
| Serie de bienvenida: nuevos miembros | Correo electrónico, push | 18 de mayo de 2026 |
| Seguimiento posterior a la compra | Correo electrónico, SMS | 14 de mayo de 2026 |
| Reparticipación de fidelización | Correo electrónico | 20 de mayo de 2026 |
| Carro abandonado: 24hr | Correo electrónico, SMS | 10 de mayo de 2026 |
| Promoción de primavera | Correo electrónico, push | 19 de mayo de 2026 |
| Win-Back: 90 días inactivos | Correo electrónico | 28 abr. 2026 |
| Recompensa de cumpleaños | Correo electrónico | 15 abr. 2026 |
| Nueva participación: exclusión push | SMS | 12 de mayo de 2026 |

Se modificaron 3 recorridos en los últimos 7 días. ¿Desea obtener detalles sobre alguno de estos?

+++


## Paso 2: Comprobar el estado de activación de la audiencia

Con los recorridos a la vista, compruebe que las audiencias que alimentan esas campañas fluyen correctamente a sus destinos.

```
Show me the activation status for the high-value loyalty segment.
```

+++Ver una respuesta de ejemplo

**Segmento de fidelidad de alto valor**: estado de activación en varios destinos:

| Destino | Estado | Última ejecución correcta | Tamaño de público |
| --- | --- | --- | --- |
| Google Ads | Activo | 21 de mayo de 2026, 02:14 AM | 48,320 |
| Meta Ads | Activo | 21 de mayo de 2026, 01:58 AM | 48,295 |
| Marketing Cloud de Salesforce | Activo | 20 de mayo de 2026, 11:30 p. m. | 47,940 |
| Adobe Target | Activo | 21 de mayo de 2026, 12:00 a. m. | 48,320 |

No se detectaron errores de flujo de datos. Todas las activaciones completadas en las últimas 3 horas.

+++


## Paso 3: Extraer métricas de rendimiento de CJA

Una vez establecido el contexto de recorrido y audiencia, utilice CJA para averiguar cómo se están convirtiendo esas campañas y dónde disminuye la participación.

```
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
```

+++Ver una respuesta de ejemplo

**Campaña de renovación de la participación por fidelidad**: del 21 de abril al 21 de mayo de 2026:

| Canal | Envíos | CTR | Conversiones | Conv. Tasa |
| --- | --- | --- | --- | --- |
| Correo electrónico | 48,320 | 8.4% | 1,973 | 4.1% |
| Push | 31,200 | 12.1% | 987 | 3.2% |

Tasa de conversión combinada: 3,8%. El CTR del correo electrónico ha aumentado un 1,2 % en comparación con el periodo de 30 días anterior. Las conversiones push son planas.

+++


## Paso 4: Sintetizar un resumen de estado de la campaña

Pida a su cliente de IA que reúna la imagen en las tres fuentes y muestre todo lo que necesite atención.

```
Give me a summary of our campaign health: what is running, which audiences are activated, and how performance looks against last month.
```

+++Ver una respuesta de ejemplo

Este es el resumen del estado de la campaña actual en AJO, Real-Time CDP y CJA:

**recorridos activos:** 8 activos, 3 modificados esta semana. El recorrido de renovación de la participación de fidelización es el que se ha actualizado más recientemente.

**Activación de audiencia:** Todos los segmentos fluyen correctamente a 4 destinos. No se detectaron errores de flujo de datos.

**Rendimiento:** el CTR de correo electrónico está subiendo en las campañas de fidelidad. La conversión push es plana. Ningún canal está en declive significativo.

**Marcas para atención:**

- El recorrido Win-Back (90 días inactivo) se modificó por última vez hace 23 días y no se ha revisado recientemente.
- La tasa de conversión push se ha mantenido sin cambios durante 3 períodos consecutivos, lo que vale la pena revisar los mensajes o el tiempo.

No se han detectado problemas críticos. Dos de los elementos anteriores merecen revisión antes del próximo lanzamiento de la campaña.

+++


Aquí es donde el enfoque de varios servidores da resultado: el cliente de IA razona en la configuración del recorrido, el estado de la audiencia y los datos de rendimiento en una sola conversación.

## Paso 5: Tome medidas sobre lo que encontró

El examen incluyó dos temas. Pida a su cliente de IA que le ayude a priorizar y enrutar cada uno.

```
For each flag you identified, what should I do and where should I go to do it?
```

+++Ver una respuesta de ejemplo

Este es un plan de acción priorizado para los dos indicadores:

**1. Recorrido Win-Back: revise las condiciones de reentrada (AJO MCP y, a continuación, la aplicación AJO si es necesario realizar cambios)**

El recorrido Win-Back no se ha modificado en 23 días. Pídeme que revise sus condiciones actuales de reentrada y lógica de salida. Si las condiciones parecen anticuadas o incorrectas, los cambios estructurales en el flujo de recorrido requieren la apertura de AJO. El límite de frecuencia y las actualizaciones de audiencia se pueden realizar aquí.

**2. Conversión push sin cambios durante 3 períodos: actualizar mensajes o probar una variante**

La conversión plana suele indicar fatiga del mensaje o una discrepancia entre la oferta y la audiencia. Dos rutas:

- **Actualizar ahora el contenido push (AEM MCP):** Si las notificaciones push se vinculan a una página de aterrizaje, agregue el servidor MCP de contenido de AEM y actualice la copia de la página o CTA sin cambiar de herramienta.
- **Ejecutar una prueba A/B push (aplicación AJO):** Cree una variante de nivel de campaña con mensajes diferentes para aislar si es contenido o segmentación. Esto requiere ir directamente a AJO.

¿Con cuál te gustaría empezar?

+++


## Lo que ha conseguido

Para realizar una revisión de estado de una campaña en canales múltiples, debe conectar AJO, Real-Time CDP y CJA a una sola sesión de IA. En lugar de abrir tres aplicaciones y ensamblar manualmente una imagen, se desplazó a través del estado del recorrido, la activación de audiencias y los datos de rendimiento en una sola conversación. El resumen sintetizado proporciona a los administradores de campaña una ruta más rápida para identificar qué está funcionando, qué necesita ajuste y dónde centrarse a continuación.

## Más cosas que puede lograr

Con AJO, CJA y Real-Time CDP conectados en la misma sesión, puede ir mucho más allá del tutorial. Expanda un escenario de abajo para ver las indicaciones que puede probar.

+++Sepa exactamente lo que se está ejecutando antes de iniciar algo nuevo

Los recorridos superpuestos, las campañas modificadas recientemente y los canales que no haya revisado pueden afectar a un nuevo inicio. Estas indicaciones le proporcionan una imagen clara del estado actual antes de agregar algo.

**Indicadores**

```
Which journey has the most active profiles right now?
```

```
Show me all journeys modified in the last 7 days.
```

```
Which campaigns are scheduled to end this week?
```

```
Are any journeys targeting the same segment as the campaign I'm about to launch?
```

+++

+++Asegúrese de que las audiencias de alcancen los destinos correctos

Los problemas de activación son silenciosos: un segmento deja de fluir y la campaña se envía a una lista más pequeña sin ninguna advertencia. Estos mensajes muestran espacios y errores antes de que afecten a los resultados.

**Indicadores**

```
Which audiences have grown the most in the last 30 days?
```

```
Are there any dataflow errors across my active destinations?
```

```
How many records were exported to each destination in the last 7 days?
```

```
Are there any audiences with no active destinations?
```

+++

+++Comprender qué está funcionando y dónde centrarse a continuación

Las tendencias de rendimiento en todos los canales le indican dónde invertir y qué puede hacer. Estas indicaciones le ayudan a identificar los resultados que impulsan y hacia dónde debería dirigirse la atención del próximo trimestre.

**Indicadores**

```
Show me email performance trends for the last 90 days.
```

```
Which campaigns are underperforming against their conversion targets?
```

```
What is the average revenue per conversion this month compared to last month?
```

```
Which channel has the highest conversion rate across all active campaigns?
```

+++


## Más información

| Recurso | Qué va a encontrar |
| --- | --- |
| [Documentación de AJO](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/ajo-home) | Documentación completa de la aplicación de AJO |
| [Documentación de MCP de Analytics](https://developer.adobe.com/analytics-mcp/docs/) | Configuración y referencia de la herramienta del MCP de CJA |
| [Documentación de MCP de Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) | Guía de configuración de RTCDP MCP |
| [Servidor MCP de AJO en el registro de IA](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) | Disponibilidad y herramientas del servidor AJO MCP |
| [Servidor MCP de CJA en el registro de IA](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | Disponibilidad y herramientas del servidor CJA MCP |
| [Servidores MCP](../tools/mcp-servers.md) | Conectar un cliente de IA a servidores MCP de Adobe |
