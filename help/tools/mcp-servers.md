---
title: Servidores MCP
description: Conecte cualquier cliente de IA compatible con MCP a los flujos de trabajo de Adobe CX Enterprise mediante los servidores de protocolo de contexto de modelo.
index: false
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: 76242d3d26596139c0ea7c2e81b698a4ef891370
workflow-type: tm+mt
source-wordcount: '2296'
ht-degree: 4%

---


# Servidores MCP

<!-- last-modified: 2026-06-09 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Los servidores MCP empresariales de Adobe CX proporcionan a cualquier cliente de IA compatible acceso directo y controlado a los datos y flujos de trabajo de Adobe. Conéctese una vez y podrá consultar el rendimiento de la campaña, activar audiencias, revisar recorridos, administrar contenido y mucho más, todo en un lenguaje sencillo, sin salir de su entorno de IA. Debido a que los servidores MCP se encuentran entre su cliente de IA y los sistemas subyacentes de Adobe, obtiene flexibilidad en lenguaje natural mientras los controles de acceso y la gobernanza de datos de su organización permanecen vigentes.

Los servidores MCP de Adobe siguen el estándar [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro) abierto. Cualquier cliente de IA compatible con MCP se conecta a cualquier servidor MCP de Adobe.

## Servidores MCP de Adobe

![El MCP de CX Enterprise conecta su cliente de IA con las herramientas de todo el conjunto de aplicaciones empresariales de Adobe CX](../assets/mcp-gateway-hero.gif)

Seleccione una aplicación para ver el extremo, las funcionalidades y las herramientas disponibles.

>[!BEGINTABS]

>[!TAB MCP de CX Enterprise]

**Un extremo. Varias aplicaciones empresariales de CX.**

Conéctese una vez y su cliente de IA tendrá acceso a las aplicaciones de CX Enterprise en función de las licencias de su organización.

```
https://cx-enterprise.adobe.io/mcp
```

| Aplicación | Lo que puede hacer | Herramientas |
| --- | --- | --- |
| Adobe Journey Optimizer | Revisar recorridos, campañas y configuraciones de canal | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Adobe Journey Optimizer B2B edition | Administre recorridos B2B, programas de cuenta, grupos de compra y personalización | TODO: validar |
| Customer Journey Analytics | Consulte informes, descubra vistas de datos y cree espacios de trabajo | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | Comprobar el estado de activación de audiencia, el estado de destino y el estado del flujo de datos | [Ver herramientas](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| Adobe Analytics | Detección de grupos de informes, creación de segmentos y creación de espacios de trabajo | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| Adobe Experience Platform | Detección de conjuntos de datos, exploración de esquemas y administración de zonas protegidas | — |

>[!TAB Experience Manager]

Adobe Experience Manager tiene varios servidores MCP para diferentes flujos de trabajo.

| Servidor MCP | Punto de conexión | Lo que puede hacer | Herramientas |
| --- | --- | --- | --- |
| [Contenido de AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | Administrar páginas, fragmentos de contenido, recursos e inicios | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [Contenido de AEM (solo lectura)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | Descubra y consulte páginas, fragmentos de contenido e inicios sin acceso de escritura | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Administrar programas, entornos, canalizaciones y repositorios | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [AEM (modo de código)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | Acceso directo de la API de REST a AEM mediante la búsqueda, lectura, escritura y eliminación en lenguaje natural | — |
| [Creación de documentos de AEM]&#x200B;(TODO: validate) | `https://mcp.adobeaemcloud.com/adobe/mcp/da` | Administrar archivos, historial de versiones y referencias de medios en la creación de documentos | — |
| [Gobernanza de AEM Experience](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | Evaluar el contenido y las imágenes en función de las directrices de marca y las reglas de conformidad | — |
| [Producción de AEM Experience](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/experience-production/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-production` | Transforme y cree páginas de AEM a escala mediante informes de contenido impulsados por IA | — |

>[!TAB Target]

El MCP de Adobe Target está en versión de beta pública. Todas las herramientas disponibles actualmente son de solo lectura. Las herramientas de escritura están planificadas para su disponibilidad general.

| Servidor MCP | Punto de conexión | Lo que puede hacer | Herramientas |
| --- | --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Revisar actividades, ofertas, audiencias, mboxes e informes de rendimiento | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/target-mcp) |

>[!TAB Marketo Engage]

>[!NOTE]
>
>Marketo Engage MCP utiliza credenciales de servicio nativas de Marketo, no de Adobe IMS. Consulte la [documentación de Marketo Engage MCP Server](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server) para obtener instrucciones sobre la configuración de autenticación.

| Servidor MCP | Punto de conexión | Lo que puede hacer | Herramientas |
| --- | --- | --- | --- |
| [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | Administrar programas, campañas, posibles clientes, listas inteligentes, correos electrónicos y formularios | TODO: validar |

>[!TAB Experience Platform]

| Servidor MCP | Punto de conexión | Lo que puede hacer | Herramientas |
| --- | --- | --- | --- |
| [Adobe Marketing Agent]&#x200B;(TODO: validar) | `https://aep-ai-ama.adobe.io/mcp` | Organice el análisis de audiencias, los diagnósticos de AEP y la creación de recorridos B2B de AJO en todas las aplicaciones de AEP | TODO: validar |

>[!TAB Workfront]

| Servidor MCP | Punto de conexión | Lo que puede hacer | Herramientas |
| --- | --- | --- | --- |
| [Adobe Workfront]&#x200B;(TODO: validar) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Administrar trabajo, proyectos, registros de planificación, perspectivas y aprobaciones de contenido | TODO: validar |

>[!ENDTABS]

## Extremos del servidor MCP

Todos los extremos se enumeran en el [Registro de Adobe AI](https://developer.adobe.com/ai-registry/?type=connector). Esta tabla es una referencia rápida: obtenga la dirección URL del punto de conexión y explore las herramientas disponibles antes de conectarse.

| Servidor | Punto de conexión | Herramientas |
| --- | --- | --- |
| [MCP de CX Enterprise](#adobe-mcp-servers) | `https://cx-enterprise.adobe.io/mcp` | · [Herramientas de Adobe Journey Optimizer](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>· [Herramientas de Customer Journey Analytics](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>· [Herramientas de Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp)<br>· [Herramientas de Adobe Analytics](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [Contenido de AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [Contenido de AEM (solo lectura)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |
| [AEM (modo de código)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | — |
| [Creación de documentos de AEM]&#x200B;(TODO: validate) | `https://mcp.adobeaemcloud.com/adobe/mcp/da` | — |
| [Gobernanza de AEM Experience](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | — |
| [Producción de AEM Experience](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/experience-production/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-production` | — |
| [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | [Ver herramientas](https://developer.adobe.com/ai-registry/#/mcp/target-mcp) |
| [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | TODO: validar |
| [Adobe Marketing Agent]&#x200B;(TODO: validar) | `https://aep-ai-ama.adobe.io/mcp` | TODO: validar |
| [Adobe Workfront]&#x200B;(TODO: validar) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | TODO: validar |

## Conexión a su cliente de IA

Todos los servidores MCP de Adobe utilizan OAuth con Adobe Identity Management Service (IMS). Seleccione la organización IMS correcta cuando se le solicite. La elección del incorrecto es la fuente más común de errores de autenticación.

Antes de realizar la configuración manualmente, compruebe en el [Registro de Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) si hay un conector administrado para el cliente de IA y la aplicación de Adobe. Los conectores administrados gestionan la autenticación automáticamente. Si hay un conector disponible para su cliente y aplicación, utilícelo en lugar de los pasos manuales que se indican a continuación.

![Un agente de IA conectándose a un servidor MCP de Adobe](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB Claude.ai]

### ![Recomendado](../assets/badge-recommended.svg) Usar un conector administrado

Vaya al [Registro de Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) y busque su aplicación de Adobe. Si aparece un conector Claude (por ejemplo, el [conector Adobe Experience Manager](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), siga sus instrucciones de configuración en lugar de los pasos siguientes.

### Conexión mediante un conector personalizado

Claude.ai admite servidores MCP remotos a través de conectores personalizados en la configuración de la cuenta.

1. Vaya a **Configuración > Integraciones**.
2. Haga clic en **Agregar conector personalizado**.
3. Escriba `https://cx-enterprise.adobe.io/mcp` como dirección URL y un nombre para mostrar como `Adobe CX Enterprise`.
4. Haz clic en **Conectar** e inicia sesión con tu Adobe ID. Seleccione la organización IMS correcta.

Configuración completa: [Documentación de conectores personalizados Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Código Claude]

### Uso de la CLI

Ejecute `claude mcp add` para registrar CX Enterprise MCP. Una conexión le permite acceder a AJO, CJA y Real-Time CDP en función de las licencias de su organización.

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### Edite el archivo de configuración

Agregue el servidor a `~/.claude.json` (global) o `.mcp.json` en la raíz del proyecto (nivel de proyecto):

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Los servidores MCP de Adobe utilizan OAuth. Claude Code le pedirá que se autentique con su Adobe ID la primera vez que llame a una herramienta. Seleccione la organización IMS correcta cuando se le solicite.

Configuración completa: [Documentación del MCP con código Claude](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursor]

Agregue CX Enterprise MCP a su archivo de configuración de Cursor `mcp.json` y después conéctese a través de **Configuración > MCP**.

- **Globales (todos los proyectos):** `~/.cursor/mcp.json`
- **Nivel de proyecto:** `.cursor/mcp.json` en la raíz del proyecto

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Una conexión le permite acceder a AJO, CJA y Real-Time CDP en función de las licencias de su organización.

Una vez agregados, los servidores MCP aparecen en **Servidores MCP instalados** en Configuración del cursor. Seleccione **Conectar** junto a cualquier servidor que muestre **Necesita autenticación** e inicie sesión con su Adobe ID. Seleccione la organización IMS que tiene acceso a la aplicación.

![Configuración del servidor MCP de cursor que muestra los servidores MCP de Adobe instalados y mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Configuración completa: [Documentación de MCP de cursor](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### ![Recomendado](../assets/badge-recommended.svg) Usar un conector administrado

Vaya al [Registro de Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) y busque su aplicación de Adobe. Si aparece un conector ChatGPT, siga sus instrucciones de configuración en lugar de los pasos a continuación.

### Conexión mediante un servidor MCP remoto

ChatGPT admite servidores MCP remotos a través del [Modo de desarrollador](https://developers.openai.com/api/docs/guides/developer-mode), disponible en los planes Pro, Plus, Business, Enterprise y Education.

1. Habilitar el modo de desarrollador en **Configuración de ChatGPT**.
2. Vaya a **Configuración > Integraciones**.
3. Haga clic en **Agregar conector personalizado** y elija **Servidor MCP remoto**.
4. Escriba `https://cx-enterprise.adobe.io/mcp` como dirección URL y `Adobe CX Enterprise` como nombre.
5. Establezca la autenticación en **OAuth**.
6. Haz clic en **Conectar** e inicia sesión con tu Adobe ID. Seleccione la organización IMS correcta.

Configuración completa: [Documentación de MCP de ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB CLI de códice OpenAI]

OpenAI Codex CLI admite servidores MCP remotos a través de la configuración TOML.

**Ubicaciones de archivos de configuración:**

- **Nivel de usuario (todos los proyectos):** `~/.codex/config.toml`
- **Ámbito del proyecto:** `.codex/config.toml` en la raíz del proyecto

Agregar MCP de CX Enterprise:

```toml
[mcp_servers.adobe-cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
enabled = true
```

Los servidores MCP de Adobe utilizan OAuth. Codex CLI gestiona el flujo de OAuth automáticamente la primera vez que se utiliza. Seleccione la organización IMS correcta cuando se le solicite.

Configuración completa: [Documentación MCP de OpenAI Codex CLI](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

Microsoft Copilot Studio se conecta a servidores MCP remotos mediante el asistente de incorporación de MCP, que crea automáticamente un conector personalizado de Power Platform.

1. Abra su agente en Copilot Studio.
2. Vaya a la página **Herramientas**.
3. Seleccione **Agregar una herramienta > Nueva herramienta > Protocolo de contexto de modelo**.
4. En el Asistente para la incorporación de MCP, introduzca:
   - **Nombre del servidor:** `Adobe CX Enterprise`
   - **URL del servidor:** `https://cx-enterprise.adobe.io/mcp`
5. Establezca la autenticación en **OAuth 2.0** y configúrelo con sus URL de autorización y token de Adobe IMS.
6. Seleccione **Crear** y después **Agregar al agente**.

>[!NOTE]
>
>Las conexiones de servidor MCP en Copilot Studio pasan por Power Platform. Se aplican las políticas de prevención de pérdida de datos (DLP) de su organización.

Configuración completa: [Documentación de Copilot Studio MCP](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Resolución de problemas

+++Cambio de organizaciones de Adobe

Si el usuario de Adobe pertenece a varias organizaciones de IMS y ve herramientas o datos para la incorrecta, desconecte el servidor MCP, cierre la sesión de Adobe en el explorador y vuelva a conectarse. Se le pedirá que elija una organización durante el inicio de sesión.

Un servidor MCP empresarial de Adobe CX solo se puede autenticar en una organización de IMS a la vez, aunque su cuenta de usuario tenga acceso a más de una.

+++

+++Especificar una zona protegida, un grupo de informes, un entorno u otro recurso de sesión

Algunos servidores MCP de Adobe CX Enterprise requieren que especifique un recurso para poder devolver resultados. Según la aplicación, puede ser una zona protegida, un programa, un entorno, un grupo de informes o una vista de datos.

Si no está seguro de a qué recursos tiene acceso, pregunte al cliente de IA. Por ejemplo: &quot;Enumerar los entornos limitados disponibles&quot; o &quot;¿A qué grupos de informes tengo acceso?&quot; Los servidores MCP de Adobe CX Enterprise suelen devolver una lista completa de los recursos disponibles para el usuario.

Una vez configurado un recurso de sesión, puede cambiarlo en cualquier momento indicando al cliente de IA cuál utilizar.

+++

+++Permisos y errores de acceso

Los clientes de IA actúan en nombre de su cuenta de usuario de Adobe mediante OAuth. Los mismos permisos y controles de acceso que se aplican cuando se inicia sesión en una aplicación de Adobe se aplican cuando se utiliza un servidor MCP.

Si una acción falla o no devuelve resultados, compruebe que el usuario tenga los permisos necesarios en Adobe Admin Console y en la aplicación CX Enterprise correspondiente. Póngase en contacto con el administrador del sistema de Adobe si necesita ajustar el acceso.

+++

+++Volver a autenticarse después de una sesión perdida

Los servidores MCP de Adobe CX Enterprise utilizan OAuth para autenticar su cuenta de usuario de Adobe. Si se pierde el estado de autenticación, no se realizarán más llamadas de herramienta hasta que se vuelva a autenticar.

Para volver a autenticar: abra la configuración del servidor MCP del cliente de IA, seleccione la entrada del servidor MCP de Adobe CX Enterprise y vuelva a conectarse. Se le pedirá que vuelva a iniciar sesión con su Adobe ID.

+++

## Herramientas agénticas en acción

Consulte Servidores MCP empresariales de Adobe CX aplicados a flujos de trabajo empresariales reales.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use CX Enterprise MCP to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use CX Enterprise MCP to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CX Enterprise MCP and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use CX Enterprise MCP for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Analizar el rendimiento de la campaña" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Analyze+Campaign+Performance" alt="Analizar el rendimiento de la campaña"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="Analizar el rendimiento de la campaña">Analizar el rendimiento de la campaña</a>
                    </p>
                    <p class="is-size-6">Utilice CX Enterprise MCP para obtener métricas de Customer Journey Analytics y datos de cualquier cliente de IA.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar tutorial</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Consultar audiencias" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Query+Audiences" alt="Consultar audiencias"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" title="Consultar audiencias">Consultar audiencias</a>
                    </p>
                    <p class="is-size-6">Utilice CX Enterprise MCP para consultar los datos de destino y audiencia de Real-Time CDP utilizando indicaciones en lenguaje sencillo.</p>
                </div>
                <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar tutorial</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="Revisar AJO recorrido" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Review+AJO+Journeys" alt="Revisar AJO recorrido"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="Revisar AJO recorrido">Revisar recorridos de AJO</a>
                    </p>
                    <p class="is-size-6">Utilice CX Enterprise MCP para acceder a los recorridos de AJO, el estado de la campaña y las condiciones de recorrido desde su cliente de IA.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar tutorial</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="Administración de contenido de AEM con IA" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI" alt="Administración de contenido de AEM con IA"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="Administración de contenido de AEM con IA">Administrar contenido de AEM con IA</a>
                    </p>
                    <p class="is-size-6">Descubra, actualice y publique páginas y fragmentos de contenido en AEM con lenguaje natural.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar tutorial</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Optimización del contenido en función de los datos de rendimiento" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data" alt="Optimización del contenido en función de los datos de rendimiento"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="Optimización del contenido en función de los datos de rendimiento">Optimizar contenido basado en datos de rendimiento</a>
                    </p>
                    <p class="is-size-6">Combine CX Enterprise MCP y AEM Content MCP Server para encontrar contenido de bajo rendimiento y actualizarlo en una sesión.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar tutorial</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/cross-channel-campaign-review.md" title="Ejecutar una revisión de campaña en canales múltiples" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="Ejecutar una revisión de campaña en canales múltiples"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="Ejecutar una revisión de campaña en canales múltiples">Ejecutar una revisión de campaña en canales múltiples</a>
                    </p>
                    <p class="is-size-6">Utilice CX Enterprise MCP para obtener una vista unificada del estado de las campañas de AJO, CJA y Real-Time CDP en una sesión de IA.</p>
                </div>
                <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Iniciar tutorial</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
