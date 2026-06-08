---
title: Optimización del contenido en función de los datos de rendimiento
description: Utilice CJA y los servidores MCP de AEM juntos para identificar el contenido de bajo rendimiento y actualizarlo, sin cambiar entre herramientas.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 3%

---


# Optimización del contenido en función de los datos de rendimiento

<!-- last-modified: 2026-05-21 -->

![Optimizar contenido basado en datos de rendimiento](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

Normalmente, cerrar el bucle entre los datos de rendimiento del contenido y las actualizaciones de contenido significa cambiar entre el análisis y el CMS. Este tutorial muestra cómo conectar Customer Journey Analytics y AEM en la misma sesión de IA, para que pueda ver páginas de bajo rendimiento y actualizarlas sin abandonar la conversación.

| | |
| --- | --- |
| Aplicaciones empresariales de CX | Customer Journey Analytics, Adobe Experience Manager as a Cloud Service |
| Herramientas agénticas | CX Enterprise MCP Gateway, AEM Content MCP Server |
| Público | Administradores de campañas, estrategas de contenido, operaciones de marketing |
| Requisito previo | cliente de IA compatible con MCP, acceso a CJA, acceso a AEM as a Cloud Service |

Cada paso muestra un mensaje representativo y un ejemplo de respuesta de IA. **Más cosas que puedes hacer** sección sigue para una exploración adicional en la misma sesión.

## Antes de empezar

>[!BEGINTABS]

>[!TAB Claude.ai]

Conecte ambos servidores MCP como conectores personalizados. Añada cada uno por separado.

1. Vaya a **Configuración > Integraciones** en Claude.ai.
2. Seleccione **Agregar conector personalizado**, escriba una dirección URL de servidor y seleccione **Conectar**.
3. Inicie sesión con su Adobe ID y, a continuación, repita para el segundo servidor.

| Servidor | Punto de conexión |
| --- | --- |
| CX Enterprise MCP Gateway | `https://cx-enterprise.adobe.io/mcp` |
| Servidor MCP de contenido de AEM | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configuración completa: [Documentación de conectores personalizados Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Conecte ambos servidores MCP mediante el modo de desarrollador de ChatGPT (se requiere plan profesional, avanzado, empresarial, o educativo). Agregue cada servidor por separado.

1. Habilitar **Modo de desarrollador** en **Configuración de ChatGPT**.
2. Vaya a **Configuración > Integraciones** y seleccione **Agregar conector personalizado > Servidor MCP remoto**.
3. Escribe una URL de servidor, selecciona **Conectar** e inicia sesión con tu Adobe ID.
4. Repita el proceso para el segundo servidor.

| Servidor | Punto de conexión |
| --- | --- |
| CX Enterprise MCP Gateway | `https://cx-enterprise.adobe.io/mcp` |
| Servidor MCP de contenido de AEM | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configuración completa: [Documentación de MCP de ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Otros clientes de IA]

¿Utiliza Gemini, Microsoft Copilot, Cursor, Claude Code u otro entorno compatible con MCP? Conéctese a ambos servidores MCP mediante estos extremos:

| Servidor | Punto de conexión |
| --- | --- |
| CX Enterprise MCP Gateway | `https://cx-enterprise.adobe.io/mcp` |
| Servidor MCP de contenido de AEM | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Instrucciones de configuración completas para todos los clientes admitidos: [Conéctese a su cliente de IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Inicie sesión con su Adobe ID cuando se le solicite y seleccione la organización de IMS vinculada a sus entornos de CJA y AEM. La elección de una organización incorrecta es la fuente más común de errores de autenticación.
>
>En la primera conexión, el cliente de IA puede pedirle que seleccione una organización de IMS o que especifique una zona protegida. Una vez establecido ese contexto, el servidor MCP lo utiliza para el resto de la sesión.
>
>Algunas herramientas le piden su aprobación antes de ejecutarse. Revise la solicitud y apruébela o rechace: no se realiza ninguna acción sin su confirmación.

## Paso 1: Identificar contenido de bajo rendimiento

Utilice CX Enterprise MCP Gateway para clasificar páginas según las métricas de participación y conversión de Customer Journey Analytics. El objetivo es una lista clara y priorizada de contenido que requiere atención.

```
Show me the 10 pages with the lowest engagement rate over the last 60 days.
```

+++Ver una respuesta de ejemplo

Páginas de participación más bajas (del 22 de marzo al 21 de mayo de 2026):

| Clasificación | Página | Tasa de participación | Tasa de rechazo | El Promedio de tiempo en la página |
| --- | --- | --- | --- | --- |
| 1 | /es/products/analytics | 8.2% | 74% | 0:42 |
| 2 | /es/resources/whitepapers | 9.1% | 71% | 0:38 |
| 3 | /es/solutions/retail | 10.4% | 69% | 0:51 |
| 4 | /en/blog/2025-q4-recap | 11.0% | 68% | 0:44 |
| 5-10 | ... | 12,3-14,1 % | 63-67 % | 0:35-1:10 |

La tasa de participación media del sitio es del 34,7 %. Estas páginas están 2-4 veces por debajo del promedio.

+++

## Paso 2: Revisar el contenido en AEM

Sin salir de la sesión de IA, extraiga el estado actual de esas páginas de AEM. Comprender lo que dice el contenido es el primer paso para saber qué cambiar.

```
Show me the current content on the /en/products/analytics page in AEM.
```

+++Ver una respuesta de ejemplo

**Página:** `/en/products/analytics`
**Última modificación:** 30 de abril de 2026 por T. MacMillan
**Estado:** Publicado

**Sección Hero:**
Titular: &quot;Decisiones basadas en datos para cada equipo&quot;
Subtítulo: &quot;Adobe Analytics proporciona a su organización información para actuar&quot;.
CTA: &quot;Solicitar una demostración&quot; → /contact/demo

**Cuerpo:** 3 bloques de características seguidos de una franja de logotipo de cliente y un CTA secundario. No hay vídeo ni elemento interactivo. La página no se ha actualizado en 21 días.

**Descripción de Meta:** &quot;Adobe Analytics: informes en tiempo real e información de IA para equipos empresariales&quot;.

+++

## Paso 3: realizar actualizaciones de destino

Con los datos de rendimiento y el contenido actual a la vista, realice actualizaciones basadas en lo que revelaron los datos.

```
Update the hero headline on the analytics product page to Make faster decisions with AI-powered analytics.
```

+++Ver una respuesta de ejemplo

**Cambio propuesto:**

| Campo | Valor actual | Nuevo valor |
| --- | --- | --- |
| Titular principal | Decisiones basadas en datos para cada equipo | Tome decisiones más rápidas con los análisis con tecnología de IA |

Página: `/en/products/analytics`

¿Confirmar este cambio? Si responde &quot;sí&quot;, la actualización se escribirá en AEM. La página permanecerá publicada en su estado actual hasta que vuelva a publicar explícitamente.

+++

>[!CAUTION]
>
>Confirme cada cambio de contenido cuando se le solicite. Revise la comparación de diferencias completa antes de aprobar las actualizaciones de las páginas activas.

## Paso 4: Validación y publicación

Cierre el bucle confirmando todos los cambios y promocionando el contenido cuando esté satisfecho con las actualizaciones.

```
Show me a summary of all changes made in this session.
```

+++Ver una respuesta de ejemplo

**Resumen de la sesión — 21 de mayo de 2026:**

| Página | Cambio | Estado |
| --- | --- | --- |
| /es/products/analytics | Titular de héroe actualizado | Guardado, sin publicar |

1 página actualizada. Listo para publicar cuando se confirme.

**Restantes de su lista de baja participación:** 9 páginas no se han actualizado en esta sesión. ¿Desea continuar con la página siguiente o crear un lanzamiento para la revisión por lotes antes de publicar?

+++

## Lo que ha conseguido

Ha conectado Customer Journey Analytics y AEM en una sola sesión de IA y ha utilizado datos de rendimiento para informar directamente a los cambios de contenido. Al pasar de una métrica a una actualización sin cambiar de herramienta, acortó el bucle de comentarios entre Analytics insight y el contenido publicado. Esto es más importante a escala de campaña, donde decenas de páginas pueden necesitar atención y los flujos de trabajo manuales entre herramientas crean retrasos.

## Más cosas que puede lograr

Los servidores MCP de CJA y AEM admiten conjuntamente todo el ciclo, desde la identificación de problemas hasta las correcciones de envío. Expanda un escenario de abajo para ver las indicaciones que puede probar en la misma sesión.

+++Encuentre el contenido que está frenando su rendimiento

El alto tráfico con baja participación indica un problema de contenido, no de tráfico. Estas indicaciones le ayudan a mostrar las páginas y los patrones específicos que requieren atención antes de que un plazo de campaña obligue al problema.

**Indicadores**

```
Show me the 10 pages with the lowest conversion rate this quarter.
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for blog posts versus product pages.
```

```
Find AEM pages that haven't been updated in over 60 days.
```

+++

+++Corrija lo que los datos le indican que corrija

Una vez que sepa qué tiene un rendimiento inferior, el siguiente paso es realizar cambios segmentados. Estas indicaciones le permiten actualizar titulares, CTA y metadescripciones en función de lo que revelaron los datos de rendimiento.

**Indicadores**

```
Update the CTA on the /en/solutions/retail page to 'See how it works'.
```

```
Add a note to the hero subheadline on the analytics page: Now with AI-powered anomaly detection.
```

```
Update the meta description on all pages in /en/products/ that contain the word 'legacy'.
```

```
Which pages updated in this session still need their CTAs reviewed?
```

+++

+++Mejoras de envíos antes de la próxima campaña

Los cambios realizados a mitad de la sesión se pueden acumular rápidamente. Estas indicaciones le ayudan a revisar lo que está listo, agrupar las actualizaciones en un lanzamiento revisable y promocionar claramente antes de que una campaña se ponga en marcha.

**Indicadores**

```
Show me all pages updated in this session that are still unpublished.
```

```
Create a launch with all changes from this session for review before publishing.
```

```
Give me a summary of all changes made in this session.
```

```
Promote everything in the current launch to production.
```

+++

## Más información

| Recurso | Qué va a encontrar |
| --- | --- |
| [Documentación de MCP de Analytics](https://developer.adobe.com/analytics-mcp/docs/) | Configuración y referencia de la herramienta del MCP de CJA |
| [Documentación de AEM as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service) | Documentación completa de AEM |
| [Servidor MCP de CJA en el registro de IA](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | Disponibilidad y herramientas del servidor CJA MCP |
| [Servidor MCP de contenido de AEM en el registro de IA](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | Disponibilidad y herramientas del servidor MCP de contenido de AEM |
| [Servidores MCP](../tools/mcp-servers.md) | Conectar un cliente de IA a servidores MCP de Adobe |
