---
title: Perspectivas de campañas de superficie sin crear informes
description: Utilice el servidor MCP de Customer Journey Analytics para hacer preguntas de rendimiento en lenguaje sencillo y obtener respuestas sin necesidad de navegar por los Report Builder.
last-substantial-update: 2026-11-16
source-git-commit: a75d5f3af3077b259da796bd381d605ae826585d
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 3%
---

# Perspectivas de campañas de superficie sin crear informes

<!-- last-modified: 2026-06-02 -->

![Plataforma de IA que muestra los siguientes pasos recomendados para mejorar el rendimiento de la campaña](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png){zoomable="yes"}

*Seleccionar para ampliar/reducir.*

El análisis de campañas que antes requería crear informes en una herramienta independiente ahora es una conversación. Este tutorial muestra cómo utilizar Coworker, o su propia plataforma de IA, con Customer Journey Analytics (CJA) y hacer preguntas de rendimiento en lenguaje sencillo. El resultado es un tiempo de ejecución de insight más rápido, sin necesidad de generar informes manualmente.

| Detalles del escenario | |
| --- | --- |
| Aplicaciones de CX Enterprise | [Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) |
| Herramientas agénticas | [Adobe CX Enterprise Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home), [Adobe CX Enterprise Coworker para plataformas de IA](../tools/mcp-servers.md#connect-to-your-ai-platform) o [Customer Journey Analytics MCP Server](../tools/mcp-servers.md) |
| Público | Analistas, administradores de campañas |
| Requisito previo | Acceso a CJA, además de Coworker, una plataforma de IA con Coworker para plataformas de IA o una plataforma de IA compatible con MCP |

Cada paso muestra un mensaje representativo y un ejemplo de respuesta de IA. **Más cosas que puedes hacer** sección sigue para una exploración adicional en la misma sesión.

## Antes de empezar

>[!BEGINTABS]

>[!TAB Coworker]

La forma más rápida de obtener estas respuestas es mediante Coworker, que no requiere ninguna configuración del servidor ni de la plataforma de IA. [Probar con el compañero](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home)

Si no puede o no quiere usar Coworker directamente, utilícelo desde su propia plataforma de IA en su lugar. Consulte la ficha **Colaborador para plataformas de IA**. Si esto tampoco funciona para usted, conecte su plataforma de IA directamente al servidor MCP de Customer Journey Analytics usando las pestañas restantes.

>[!TAB Colaborador para plataformas de IA]

También puede completar este tutorial con Coworker para plataformas de IA desde su propia plataforma de IA. [Configurar compañero para plataformas de IA](../tools/mcp-servers.md#connect-to-your-ai-platform) | [Documentación de Adobe](https://experienceleague.adobe.com/en/docs/coworker/content/ai-platforms#set-up-coworker)

>[!TAB Claude.ai]

Conecte el servidor MCP de Customer Journey Analytics como un conector personalizado.

1. Vaya a **Configuración > Integraciones** en Claude.ai.
2. Seleccione **Agregar conector personalizado** e introduzca la dirección URL del servidor: `https://cja-mcp.adobe.io/mcp`
3. Seleccione **Conectar** e inicie sesión con su Adobe ID.

Configuración completa: [Documentación de conectores personalizados Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Conecte el servidor MCP de Customer Journey Analytics mediante el modo de desarrollador de ChatGPT (se requiere plan profesional, avanzado, empresarial, o educativo).

1. Habilitar **Modo de desarrollador** en **Configuración de ChatGPT**.
2. Vaya a **Configuración > Integraciones** y seleccione **Agregar conector personalizado > Servidor MCP remoto**.
3. Escriba la dirección URL del servidor: `https://cja-mcp.adobe.io/mcp`
4. Seleccione **Conectar** e inicie sesión con su Adobe ID.

Configuración completa: [Documentación de MCP de ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Otras plataformas de IA]

¿Utiliza Gemini, Microsoft Copilot, Cursor, Claude Code u otro entorno compatible con MCP? Conéctese al servidor MCP de Customer Journey Analytics mediante este extremo:

```
https://cja-mcp.adobe.io/mcp
```

Instrucciones de configuración completas para todas las plataformas de IA compatibles: [Conéctese a su plataforma de IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Inicie sesión con su Adobe ID cuando se le solicite y seleccione la organización de IMS vinculada a sus vistas de datos de CJA. La elección de una organización incorrecta es la fuente más común de errores de autenticación.
>
>En la primera conexión, la plataforma de IA puede pedirle que seleccione una organización de IMS o que especifique una zona protegida. Una vez establecido ese contexto, el servidor MCP lo utiliza para el resto de la sesión.
>
>Algunas herramientas le piden su aprobación antes de ejecutarse. Revise la solicitud y apruébela o rechace. No se realiza ninguna acción sin su confirmación.

## Paso 1: Descubra las vistas de datos disponibles

Comience por pedirle a su plataforma de IA que enumere las vistas de datos disponibles en su cuenta de CJA. Esto indica a qué conjuntos de datos puede consultar antes de ejecutar cualquier informe.

```
What data views are available in my CJA account?
```

+++Ver una respuesta de ejemplo

![Vistas de datos de CJA disponibles en el listado de la plataforma AI](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step1-data-views.png){zoomable="yes"}

*Seleccionar para ampliar/reducir.*

+++


## Paso 2: Extraer datos de rendimiento de la campaña

Con una vista de datos identificada, solicite el rendimiento de la campaña por ingresos y tasa de conversión. La API resuelve los nombres de métricas y dimensiones de la vista de datos sin requerir ID técnicos.

```
For '[data view name]', show me the top campaigns by revenue and conversion rate for the last 30 days.
```

+++Ver una respuesta de ejemplo

![Plataforma de IA que muestra las principales campañas según los ingresos y la tasa de conversión de la vista de datos omnicanal - de varias industrias](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step2.gif){zoomable="yes"}

*Seleccionar para ampliar/reducir.*

+++


>[!NOTE]
>
>Reemplace `[data view name]` con el nombre de su vista de datos del paso 1. Compruebe los resultados en Analysis Workspace utilizando la misma vista de datos e intervalo de fechas antes de compartirlos con las partes interesadas.

## Paso 3: Identificar qué es lo que impulsa el rendimiento

Solicite a su plataforma de IA que explique qué es lo que impulsa las diferencias de rendimiento entre grupos de campañas. Esto pasa de los números de titulares a las variables subyacentes.

```
What factors are driving the results for these campaign groups?
```

+++Ver una respuesta de ejemplo

![Plataforma de IA que explica los factores que impulsan el rendimiento del grupo de campañas](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step3.gif){zoomable="yes"}

*Seleccionar para ampliar/reducir.*

+++


## Paso 4: Profundizar en un tipo de campaña específico

Haga un seguimiento de un resultado específico solicitando un desglose de nivel de segmento. Esto revela qué tipos de clientes están impulsando el rendimiento dentro de un tipo de campaña.

```
Break down Promotional Email Campaigns by Customer Segment and explain what's driving the high conversion rate.
```

+++Ver una respuesta de ejemplo

![La plataforma de IA desglosa el rendimiento de la campaña de correo electrónico promocional por segmento de cliente](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step4-segment-breakdown.png){zoomable="yes"}

*Seleccionar para ampliar/reducir.*

+++


## Paso 5: Tome medidas sobre lo que encontró

Pida recomendaciones priorizadas basadas en todo lo que ha aparecido en la sesión. Solicitar estimaciones del valor comercial le ayuda a decidir dónde actuar primero.

```
Based on these findings, recommend the highest-impact actions to increase revenue and conversion rates. Prioritize recommendations by expected business value and estimate the potential uplift.
```

+++Ver una respuesta de ejemplo

![Plataforma de IA que recomienda acciones priorizadas con valor comercial estimado](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5.gif){zoomable="yes"}

*Seleccionar para ampliar/reducir.*

+++


>[!NOTE]
>
>Las herramientas de CJA pueden crear segmentos, métricas calculadas y proyectos de Workspace en CJA en la misma sesión. Para actualizar campañas, recorridos o contenido en otras aplicaciones, conecte el servidor MCP correspondiente o vaya directamente a la aplicación.

## Lo que ha conseguido

Utilizó Coworker o su plataforma de IA con Customer Journey Analytics y pasó de la detección de vistas de datos a las recomendaciones empresariales priorizadas en cinco mensajes. Ha identificado las campañas principales por ingresos y tasa de conversión, ha descubierto los factores que impulsan el rendimiento en los grupos de campañas, ha profundizado en los detalles de nivel de segmento para un tipo de campaña específico y ha recibido recomendaciones de clasificación con un aumento estimado. Este enfoque reemplaza la creación de informes con una conversación directa, lo que reduce el tiempo entre una pregunta comercial y un plan de acción respaldado por datos.

## Más cosas que puede lograr

El servidor MCP de Customer Journey Analytics puede mostrar muchas más perspectivas que las que se explican en el tutorial. Expanda un escenario de abajo para ver las indicaciones que puede probar en la misma sesión.

+++Encuentre lo que funciona y lo que no

Una idea rápida de qué campañas se están entregando y cuáles no le ayuda a enfocar el esfuerzo antes de revisar cualquier informe detallado. Estas indicaciones le muestran esa imagen en una sesión.

**Indicadores**

```
Which campaigns are driving the most revenue and conversions?
```

```
Show me the campaigns that need attention this month.
```

```
What channels are outperforming expectations?
```

```
Identify the biggest performance changes compared to last month.
```

```
Show me conversion performance by traffic source.
```

+++

+++Comprender lo que genera resultados

Las métricas de titular indican lo que ha sucedido. Estas indicaciones le ayudan a comprender por qué: qué segmentos, canales y puntos de contacto están detrás de los números.

**Indicadores**

```
What factors are driving revenue growth?
```

```
Explain why conversion rates changed this quarter.
```

```
Break down campaign performance by customer segment.
```

```
Which customer segments are growing fastest?
```

```
Which touchpoints contribute most to conversions?
```

+++

+++Descubra oportunidades de crecimiento

Saber dónde está el rendimiento es fuerte es sólo la mitad del panorama. Estas indicaciones le ayudan a identificar dónde puede invertir más, qué audiencias tienen margen de ampliación y qué campañas están listas para escalar.

**Indicadores**

```
Where should we invest more marketing budget?
```

```
Which audiences have the greatest growth potential?
```

```
Which campaigns should we scale?
```

```
What would have the biggest impact on revenue?
```

+++

+++Convierta perspectivas en acción

Las herramientas de CJA pueden crear segmentos, audiencias, métricas calculadas y proyectos de Workspace directamente en CJA sin abandonar la sesión de IA. Utilice estas indicaciones para actuar sobre lo que ha encontrado.

**Indicadores**

```
Create a segment for high-value customers.
```

```
Build an audience from recent purchasers.
```

```
Create a calculated metric for conversion efficiency.
```

```
Save this analysis as a Workspace project for executive reporting.
```

+++


## Más información

| Recurso | Qué va a encontrar |
| --- | --- |
| [Servidor MCP de CJA en el registro de IA](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | Disponibilidad y herramientas del servidor CJA MCP |
| [Documentación de Customer Journey Analytics](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-landing){target="_blank"} | Documentación completa de la aplicación de CJA |
