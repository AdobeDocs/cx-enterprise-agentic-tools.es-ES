---
title: Servidores MCP
description: Conecte cualquier cliente de IA compatible con MCP a los flujos de trabajo de Adobe CX Enterprise mediante los servidores de protocolo de contexto de modelo.
last-substantial-update: 2026-09-16
source-git-commit: a70eede6e0efe0d1dbdc00c5d9de5aeb3b5d75de
workflow-type: tm+mt
source-wordcount: '2400'
ht-degree: 6%
---

# Servidores MCP

<!-- last-modified: 2026-09-16 -->

Los servidores MCP de Adobe proporcionan a cualquier cliente de IA compatible acceso directo y controlado a los datos y flujos de trabajo de Adobe. Conéctese una vez y podrá consultar el rendimiento de la campaña, activar audiencias, revisar recorridos, administrar contenido y mucho más, todo en un lenguaje sencillo, sin salir de su entorno de IA. Debido a que los servidores MCP se encuentran entre su cliente de IA y los sistemas subyacentes de Adobe, obtiene flexibilidad en lenguaje natural mientras los controles de acceso y la gobernanza de datos de su organización permanecen vigentes.

Los servidores MCP de Adobe siguen el estándar [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro) abierto. Cualquier cliente de IA compatible con MCP se conecta a cualquier servidor MCP de Adobe.

## Servidores MCP de CX Enterprise {#cx-enterprise-mcp-servers}

>[!CONTEXTUALHELP]
>id="cx-enterprise-agentic-tools_mcp_servers_cx-enterprise"
>title="CX Enterprise Coworker"
>abstract="Pregunte, analice y tome medidas en sus aplicaciones de CX Enterprise en un lenguaje sencillo, sin necesidad de configurar el servidor. Para aplicaciones individuales con su propio servidor MCP, conéctese directamente en su lugar."
>additional-url="https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home" text="Documentación de CX Enterprise Coworker"

![CX Enterprise Coworker conecta un cliente de IA a las aplicaciones de CX Enterprise](../assets/mcp-sub-hero.gif)

**La forma más rápida de trabajar en todas las aplicaciones de CX Enterprise es CX Enterprise Coworker.** Se conecta a sus aplicaciones empresariales de CX sin configuración de servidor, sin punto final para registrar y sin configuración de cliente de IA. [Probar CX Enterprise Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home)

Si prefiere conectar su propio cliente de IA directamente a una aplicación de Adobe específica, varias aplicaciones también tienen su propio servidor MCP.

| Servidor MCP | Punto de conexión | Lo que puede hacer | También a través de CX Enterprise Coworker |
| --- | --- | --- | --- |
| [Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/ajo-mcp) | `https://ajo-mcp.adobe.io/mcp` | Revisar recorridos, campañas y configuraciones de canal | Sí |
| [Customer Journey Analytics](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/cja-mcp) | `https://cja-mcp.adobe.io/mcp` | Consulte informes, descubra vistas de datos y cree espacios de trabajo | Sí |
| [Adobe Analytics](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/analytics-mcp) | `https://aa-mcp.adobe.io/mcp` | Detección de grupos de informes, creación de segmentos y creación de espacios de trabajo | Sí |
| [Adobe Target](https://experienceleague.adobe.com/es/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Revise actividades, ofertas, audiencias, mboxes, informes de rendimiento y direcciones URL de vista previa (beta pública: las herramientas son de solo lectura y las herramientas de escritura están planificadas para su disponibilidad general) | Sí |
| [Real-Time CDP](https://experienceleague.adobe.com/es/docs/experience-platform/rtcdp/intro/rtcdp-mcp) | `https://rtcdp-mcp.adobe.io/mcp` | Buscar audiencias, destinos, fuentes y ejecuciones de flujo; inspeccionar áreas de nombres de identidad y políticas de combinación (beta pública: se requiere lista de permitidos, todas las herramientas son de solo lectura) | Sí |
| [Servidor MCP de AEM](https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/mcp-servers/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | Administrar páginas, fragmentos de contenido, activos y lanzamientos; evaluar contenido e imágenes con respecto a las directrices de marca y las reglas de conformidad | Sí |
| [AEM Cloud Manager](https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Administrar programas, entornos, canalizaciones y repositorios | No |
| Adobe Marketing Agent | `https://aep-ai-ama.adobe.io/mcp` | Organice el análisis de audiencias, los diagnósticos de AEP y la creación de recorridos B2B de AJO en todas las aplicaciones de AEP | No |
| [Adobe Workfront](https://experienceleague.adobe.com/es/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Administrar trabajo, proyectos, registros de planificación, perspectivas y aprobaciones de contenido | No |
| [Marketo Engage](https://experienceleague.adobe.com/es/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | Administre formularios, campañas inteligentes, posibles clientes, listas, programas, correos electrónicos y operaciones por lotes | Sí |
| Adobe Experience Platform | Mediante [CX Enterprise Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home) | Detección de conjuntos de datos, exploración de esquemas y administración de zonas protegidas | N/D |
| Campaign Classic | Mediante [CX Enterprise Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home) | Detección de instancias de Campaign, exploración de esquemas, ejecución de consultas, control de flujo de trabajo y ejecución de SOAP/JS | N/D |
| Experimentación | Mediante [CX Enterprise Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home) | Informes de experimentos A/B, MVT y MAB, métricas, perspectivas, oportunidades y planificación de tamaño de muestra | N/D |
| GenStudio for Performance Marketing | Mediante [CX Enterprise Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home) | Acceso a datos de rendimiento de publicidad y perspectivas creativas | N/D |
| Adobe Journey Optimizer B2B edition | Mediante [CX Enterprise Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home) | Administre recorridos B2B, programas de cuenta, grupos de compra y personalización | N/D |

>[!NOTE]
>
>El acceso a cada servidor MCP depende de los derechos de su organización para esa aplicación y de los permisos del usuario dentro de ella. Las últimas cinco filas aún no tienen su propio servidor MCP disponible para la conexión directa. Utilice CX Enterprise Coworker para ponerse en contacto con ellos hoy mismo.

## Conexión a su cliente de IA

La mayoría de los servidores MCP de Adobe utilizan OAuth con Adobe Identity Management Service (IMS). Seleccione la organización IMS correcta cuando se le solicite. La elección del incorrecto es la fuente más común de errores de autenticación.

![Un agente de IA conectándose a un servidor MCP de Adobe](../assets/hero-connect-mcp-servers.gif)

Si utiliza CX Enterprise Coworker, estas conexiones se producen automáticamente. Nada de lo siguiente se aplica a usted. Los pasos siguientes sirven para conectar su propio cliente de IA directamente a un servidor MCP de Adobe y utilizar el punto final del servidor MCP de AEM como ejemplo. El mismo proceso se aplica a cualquier servidor MCP de Adobe: cambie la URL del punto de conexión por el servidor al que desee conectarse.

>[!BEGINTABS]

>[!TAB CX Enterprise Coworker]

CX Enterprise Coworker ya incluye muchas de estas funcionalidades de MCP. No hay ningún servidor que agregar, ningún extremo que registrar ni ningún cliente de IA que configurar. Inicie sesión en CX Enterprise Coworker y estará listo para usar.

Documentación completa: [Documentación de CX Enterprise Coworker](https://experienceleague.adobe.com/es/docs/cx-enterprise-coworker/content/home)

>[!TAB Claude.ai]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Recomendado">: usar un conector administrado

Vaya al [Registro de Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) y busque su aplicación de Adobe. Si aparece un conector Claude (por ejemplo, el [conector Adobe Experience Manager](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), siga sus instrucciones de configuración en lugar de los pasos siguientes.

### Conexión mediante un conector personalizado

Claude.ai admite servidores MCP remotos a través de conectores personalizados en la configuración de la cuenta.

1. Vaya a **Configuración > Integraciones**.
2. Haga clic en **Agregar conector personalizado**.
3. Escriba el extremo del servidor como la dirección URL (por ejemplo, `https://mcp.adobeaemcloud.com/adobe/mcp/aem` para el servidor MCP de AEM) y un nombre para mostrar de su elección.
4. Haz clic en **Conectar** e inicia sesión con tu Adobe ID. Seleccione la organización IMS correcta.

Configuración completa: [Documentación de conectores personalizados Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Código Claude]

### Uso de la CLI

Ejecute `claude mcp add` para registrar un servidor MCP de Adobe. Reemplace el nombre y la dirección URL del servidor por los valores del servidor al que desea conectarse. Este ejemplo utiliza el servidor MCP de AEM:

```bash
claude mcp add --transport http adobe-aem https://mcp.adobeaemcloud.com/adobe/mcp/aem
```

### Edite el archivo de configuración

Agregue el servidor a `~/.claude.json` (global) o `.mcp.json` en la raíz del proyecto (nivel de proyecto). Reemplace la clave y la dirección URL por los valores del servidor al que desea conectarse:

```json
{
  "mcpServers": {
    "adobe-aem": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/aem"
    }
  }
}
```

Los servidores MCP de Adobe utilizan OAuth. Claude Code le pedirá que se autentique con su Adobe ID la primera vez que llame a una herramienta. Seleccione la organización IMS correcta cuando se le solicite.

Configuración completa: [Documentación del MCP con código Claude](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursor]

Agregue un servidor MCP de Adobe al archivo de configuración del cursor `mcp.json` y, a continuación, conéctese mediante **Configuración > MCP**. Reemplace la clave y la dirección URL por los valores del servidor al que desea conectarse. Este ejemplo utiliza el servidor MCP de AEM:

- **Globales (todos los proyectos):** `~/.cursor/mcp.json`
- **Nivel de proyecto:** `.cursor/mcp.json` en la raíz del proyecto

```json
{
  "mcpServers": {
    "adobe-aem": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/aem"
    }
  }
}
```

Una vez agregados, los servidores MCP aparecen en **Servidores MCP instalados** en Configuración del cursor. Seleccione **Conectar** junto a cualquier servidor que muestre **Necesita autenticación** e inicie sesión con su Adobe ID. Seleccione la organización IMS que tiene acceso a la aplicación.

![Configuración del servidor MCP de cursor que muestra los servidores MCP de Adobe instalados y mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Configuración completa: [Documentación de MCP de cursor](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Recomendado">: usar un conector administrado

Vaya al [Registro de Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) y busque su aplicación de Adobe. Si aparece un conector ChatGPT, siga sus instrucciones de configuración en lugar de los pasos a continuación.

### Conexión mediante un servidor MCP remoto

Pida al administrador de ChatGPT que añada el servidor MCP para su organización. Esto permite que todos los usuarios se conecten sin la configuración siguiente.

Si un administrador no puede agregarla o solo desea la conexión para su cuenta, siga estos pasos.

**Configuración única:** active el modo de desarrollador para poder registrar una dirección URL de MCP personalizada.

1. Vaya a **Configuración > Seguridad e inicio de sesión**.
2. Activar **modo de desarrollador**.

**Agregar un servidor:**

1. Vaya a **Configuración > Complementos > Examinar complementos**.
2. Seleccione **+** para agregar un nuevo complemento.
3. Escriba un nombre, por ejemplo `AEM Content AI` o `Adobe Journey Optimizer`.
4. Introduzca una descripción.
5. Seleccione **URL del servidor**.
6. En **Conexión**, escriba la dirección URL completa de MCP de Adobe. Por ejemplo, `https://mcp.adobeaemcloud.com/adobe/mcp/aem` para AEM o `https://ajo-mcp.adobe.io/mcp` para Adobe Journey Optimizer.
7. Establezca **Autenticación** en **OAuth**.
8. Lea y acepte los términos de servicio.
9. Seleccione **Crear**.
10. Inicie sesión con la cuenta de Adobe que tiene acceso a la aplicación CX Enterprise a la que se conecta el servidor MCP.

Configuración completa: [Documentación de MCP de ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB CLI de códice OpenAI]

OpenAI Codex CLI admite servidores MCP remotos a través de la configuración TOML.

**Ubicaciones de archivos de configuración:**

- **Nivel de usuario (todos los proyectos):** `~/.codex/config.toml`
- **Ámbito del proyecto:** `.codex/config.toml` en la raíz del proyecto

Reemplace el nombre de sección y la dirección URL por los valores del servidor al que desea conectarse. Este ejemplo utiliza el servidor MCP de AEM:

```toml
[mcp_servers.adobe-aem]
url = "https://mcp.adobeaemcloud.com/adobe/mcp/aem"
enabled = true
```

Los servidores MCP de Adobe utilizan OAuth. Codex CLI gestiona el flujo de OAuth automáticamente la primera vez que se utiliza. Seleccione la organización IMS correcta cuando se le solicite.

Configuración completa: [Documentación MCP de OpenAI Codex CLI](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

Microsoft Copilot Studio se conecta a servidores MCP remotos mediante el asistente de incorporación de MCP, que crea automáticamente un conector personalizado de Power Platform.

1. Abra su agente en Copilot Studio.
2. Vaya a la página **Herramientas**.
3. Seleccione **Agregar una herramienta > Nueva herramienta > Protocolo de contexto de modelo**.
4. En el Asistente para la incorporación de MCP, introduzca los detalles del servidor. Por ejemplo, para el servidor MCP de AEM:
   - **Nombre del servidor:** `AEM`
   - **URL del servidor:** `https://mcp.adobeaemcloud.com/adobe/mcp/aem`
5. Establezca la autenticación en **OAuth 2.0** y configúrelo con sus URL de autorización y token de Adobe IMS.
6. Seleccione **Crear** y después **Agregar al agente**.

>[!NOTE]
>
>Las conexiones de servidor MCP en Copilot Studio pasan por Power Platform. Se aplican las políticas de prevención de pérdida de datos (DLP) de su organización.

Configuración completa: [Documentación de Copilot Studio MCP](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Servidores MCP en acción

Vea cómo los servidores MCP de Adobe se ponen a trabajar en problemas empresariales reales. Cada tutorial parte de un auténtico desafío operativo y muestra cómo un cliente de IA lo resuelve en lenguaje sencillo, sin cambiar de herramienta ni escribir código.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* ../use-cases/query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* ../use-cases/manage-ajo-journeys.md
  {title = Catch journey issues early}
  {description = Monitor active journeys and surface operational issues before they reach your audience.}
  {cta = Monitor your journeys}

* ../use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Close content performance gaps}
  {description = Surface conversion gaps in CJA, trace them to underperforming content in AEM, and apply the fix in a single AI session.}
  {cta = Close performance gaps}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Perspectivas de campaña sin informes">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Perspectivas de campaña sin informes"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" title="Perspectivas de campaña sin informes">Perspectivas de campaña sin informes</a>
                    </p>
                    <p class="is-size-6">Haga preguntas de rendimiento en lenguaje sencillo y obtenga respuestas de Customer Journey Analytics, sin crear un solo informe.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Perspectivas de la campaña de Surface</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience activation at a glance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Generalidades de Audience activation">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Generalidades de Audience activation"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="Generalidades de Audience activation">Generalidades de activación de audiencia</a>
                    </p>
                    <p class="is-size-6">Vea qué audiencias están activas, a dónde fluyen y si los destinos están en buen estado, sin navegar por Real-Time CDP.</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Comprobar activación de audiencia</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Catch journey issues early">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="Detectar problemas de recorrido antes">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="Detectar problemas de recorrido antes"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" title="Detectar problemas de recorrido antes">Detectar problemas de recorrido antes</a>
                    </p>
                    <p class="is-size-6">Supervise los recorridos activos y los problemas operativos antes de que lleguen a su audiencia.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Supervise sus recorridos</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="Envío de actualizaciones de contenido más rápido">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Envío de actualizaciones de contenido más rápido"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" title="Envío de actualizaciones de contenido más rápido">Enviar actualizaciones de contenido más rápido</a>
                    </p>
                    <p class="is-size-6">Busque, actualice y publique páginas de AEM y fragmentos de contenido más rápido, sin cambiar a la interfaz de AEM.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Enviar contenido más rápido</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Close content performance gaps">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Cerrar brechas de rendimiento de contenido">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="Cerrar brechas de rendimiento de contenido"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" title="Cerrar brechas de rendimiento de contenido">Cerrar brechas de rendimiento de contenido</a>
                    </p>
                    <p class="is-size-6">Elimine los huecos de conversión en CJA, rastree el contenido con bajo rendimiento en AEM y aplique la corrección en una sola sesión de IA.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Cerrar brechas de rendimiento</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## ¿Necesita más ayuda?

Las conexiones MCP implican autenticación, selección de la organización y permisos de nivel de aplicación. Si algo no funciona como se espera, estos pasos cubren las causas más comunes.

+++Cambio de organizaciones de Adobe

Si el usuario de Adobe pertenece a varias organizaciones de IMS y ve herramientas o datos para la incorrecta, desconecte el servidor MCP, cierre la sesión de Adobe en el explorador y vuelva a conectarse. Se le pedirá que elija una organización durante el inicio de sesión.

Un servidor MCP de Adobe solo se puede autenticar en una organización IMS a la vez, aunque su cuenta de usuario tenga acceso a más de una.

+++

+++Especificar una zona protegida, un grupo de informes, un entorno u otro recurso de sesión

Algunos servidores MCP de Adobe requieren que especifique un recurso para que puedan devolver resultados. Según la aplicación, puede ser una zona protegida, un programa, un entorno, un grupo de informes o una vista de datos.

Si no está seguro de a qué recursos tiene acceso, pregunte al cliente de IA. Por ejemplo: &quot;Enumerar los entornos limitados disponibles&quot; o &quot;¿A qué grupos de informes tengo acceso?&quot; Los servidores MCP de Adobe suelen devolver una lista completa de los recursos disponibles para el usuario.

Una vez configurado un recurso de sesión, puede cambiarlo en cualquier momento indicando al cliente de IA cuál utilizar.

+++

+++Permisos y errores de acceso

Los clientes de IA actúan en nombre de su cuenta de usuario de Adobe mediante OAuth. Los mismos permisos y controles de acceso que se aplican cuando se inicia sesión en una aplicación de Adobe se aplican cuando se utiliza un servidor MCP.

Si una acción falla o no devuelve resultados, compruebe que el usuario tenga los permisos necesarios en Adobe Admin Console y en la aplicación CX Enterprise correspondiente. Póngase en contacto con el administrador del sistema de Adobe si necesita ajustar el acceso.

+++

+++Volver a autenticarse después de una sesión perdida

Los servidores MCP de Adobe utilizan OAuth para autenticar la cuenta de usuario de Adobe. Si se pierde el estado de autenticación, no se realizarán más llamadas de herramienta hasta que se vuelva a autenticar.

Para volver a autenticar: abra la configuración del servidor MCP del cliente de IA, seleccione la entrada del servidor MCP de Adobe y vuelva a conectarse. Se le pedirá que vuelva a iniciar sesión con su Adobe ID.

+++
