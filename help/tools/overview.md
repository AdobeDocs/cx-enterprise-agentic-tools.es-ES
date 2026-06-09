---
title: Herramientas de agente
description: Compare servidores MCP, habilidades de agente y API para generadores y elija la herramienta original adecuada para sus flujos de trabajo empresariales de Adobe CX.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: 76a2dc291781d0555e0b128eb6c0e226759f5cc8
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 0%

---


# Herramientas de agente

<!-- last-modified: 2026-06-08 -->

No todas las herramientas agénticas tienen la misma necesidad. Explore qué hace cada uno, cuándo usarlo y cómo empezar, para que pueda elegir el punto de partida adecuado para su situación.

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI client to Adobe CX Enterprise data and workflows. No coding required.}
  {cta = Explore MCP Servers}
  {image = ../assets/mcp-servers-card.png}

* agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflow instructions that guide agents through CX Enterprise tasks consistently.}
  {cta = Explore Agent Skills}
  {image = ../assets/agent-skills-card.png}

* apis.md
  {title = APIs for Builders}
  {description = Build custom applications and integrations using the same APIs that power Adobe products.}
  {cta = Explore APIs for Builders}
  {image = ../assets/apis-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="mcp-servers.md" title="Servidores MCP">
                        <img class="is-bordered-r-small" src="../assets/mcp-servers-card.png" alt="Servidores MCP"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="mcp-servers.md" title="Servidores MCP">Servidores MCP</a>
                    </p>
                    <p class="is-size-6">Conecte cualquier cliente de IA compatible a los datos y flujos de trabajo de Adobe CX Enterprise. No se requiere codificación.</p>
                </div>
                <a href="mcp-servers.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorar servidores MCP</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="agent-skills.md" title="Aptitudes de agente">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="Aptitudes de agente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="agent-skills.md" title="Aptitudes de agente">Aptitudes de agente</a>
                    </p>
                    <p class="is-size-6">Instrucciones de flujo de trabajo revisadas por Adobe que guían a los agentes a través de las tareas de CX Enterprise de forma coherente.</p>
                </div>
                <a href="agent-skills.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorar las aptitudes del agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="apis.md" title="API para generadores">
                        <img class="is-bordered-r-small" src="../assets/apis-card.png" alt="API para generadores"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="apis.md" title="API para generadores">API para generadores</a>
                    </p>
                    <p class="is-size-6">Cree aplicaciones e integraciones personalizadas con las mismas API que alimentan los productos de Adobe.</p>
                </div>
                <a href="apis.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorar API para generadores</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## Comparar herramientas agénticas

| | Servidores MCP | Aptitudes de agente | API para generadores |
| --- | --- | --- | --- |
| Mejor para | Usuarios de aplicaciones empresariales de CX | Usuarios y desarrolladores de aplicaciones empresariales de CX | Desarrolladores |
| Requiere codificación | No | No | Sí |
| Tiempo de configuración | Minutes | Minutes | Horas a días |
| Lo que obtienes | Acceso a aplicaciones empresariales CX desde sus clientes de IA | Flujos de trabajo guiados y repetibles | Control programático completo |

## ¿No estás seguro de por dónde empezar?

- Para usar IA para interactuar con aplicaciones de CX Enterprise (realizar acciones, consultar datos y permitir que la IA descubra qué hacer después a través de una conversación natural), [Servidores MCP](mcp-servers.md) son el punto de partida más flexible.
- Para que los agentes sigan de manera consistente las prácticas recomendadas de Adobe para los flujos de trabajo de CX Enterprise sin improvisar, [Agent Skills](agent-skills.md) codifican esa experiencia de dominio en instrucciones reutilizables.
- Para crear una aplicación enfocada que optimiza o automatiza un flujo de trabajo empresarial de CX específico para sus usuarios, las [API para generadores](apis.md) le proporcionan control directo y programable sobre exactamente lo que sucede.

>[!BEGINTABS]

>[!TAB Servidores MCP]

Piense en los servidores MCP como un cable activo entre su cliente de IA y las aplicaciones empresariales de CX. Conéctese una vez y su IA podrá consultar campañas, extraer audiencias, comprobar el estado del recorrido y mucho más, todo en un lenguaje sencillo, sin necesidad de código.

**Usar servidores MCP cuando:**

- Desea integrar la IA directamente en sus flujos de trabajo de CX Enterprise
- Desea que los datos de CX Enterprise se encuentren dentro del cliente de IA que ya utiliza
- Está realizando análisis exploratorios o recuperación de datos ad hoc
- Desea obtener resultados rápidamente, sin dar vueltas a un proyecto

[Explorar servidores MCP](mcp-servers.md)

>[!TAB Aptitudes de agente]

Las habilidades de agente son conocimientos de dominio de Adobe, codificados como instrucciones que el agente puede seguir. En lugar de esperar que su agente descubra los pasos correctos, una habilidad le dice exactamente qué hacer, de forma fiable, repetida y ya ajustada para los flujos de trabajo de CX Enterprise.

**Usar aptitudes de agente cuando:**

- Desea seguir las prácticas recomendadas de Adobe al realizar trabajo en aplicaciones de CX Enterprise a través de clientes de IA
- Desea que la misma tarea se realice de la misma manera cada vez
- Está ejecutando flujos de trabajo de producción de contenido o medios repetibles

[Explorar aptitudes del agente](agent-skills.md)

>[!TAB API para generadores]

Las API son los componentes básicos. Proporcionan a los desarrolladores acceso directo y programático a los datos y las operaciones de Adobe, utilizando las mismas API que alimentan los productos propios de Adobe. Utilícelos para crear experiencias personalizadas centradas que optimicen flujos de trabajo empresariales específicos con las barreras que necesita su organización.

**Usar API cuando:**

- Está creando una aplicación o integración personalizada para un caso de uso empresarial específico
- Debe optimizar o automatizar un flujo de trabajo con protecciones y controles específicos
- Utiliza el código o cursor Claude para generar una aplicación completa
- Debe integrar los datos de CX Enterprise en otro sistema

[Explorar las API para generadores](apis.md)

>[!ENDTABS]

## Usándolos juntos.

Estas herramientas están diseñadas para funcionar juntas. Al combinarlos, es donde puede obtener el máximo rendimiento de Adobe AI. Las habilidades de agente pueden guiar la forma en que un cliente de IA utiliza los servidores MCP, lo que mantiene a los agentes en el camino correcto para los flujos de trabajo de CX Enterprise. Las habilidades también pueden informar de cómo y cuándo llamar a las API de, lo que agrega protecciones de prácticas recomendadas de Adobe a las automatizaciones creadas a medida. No tienes que elegir solo una.

## Herramientas agénticas en acción

Consulte estas herramientas aplicadas a flujos de trabajo empresariales de CX reales.

<!--
CARDS

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Try with MCP}

* https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

* https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app
  {title = Invoke AEM APIs from a web app}
  {description = Build a web application that authenticates users and calls AEM OpenAPIs using OAuth to deliver governed, programmatic access.}
  {cta = Try with APIs}
  {image = ../assets/using-api-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Consultar audiencias">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Consultar audiencias"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="Consultar audiencias">Consultar audiencias</a>
                    </p>
                    <p class="is-size-6">Utilice CX Enterprise MCP para consultar los datos de destino y audiencia de Real-Time CDP utilizando indicaciones en lenguaje sencillo.</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Probar con MCP</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Develop AEM components with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" title="Desarrollo de componentes de AEM con IA" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="Desarrollo de componentes de AEM con IA"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" title="Desarrollo de componentes de AEM con IA">Desarrollar componentes de AEM con IA</a>
                    </p>
                    <p class="is-size-6">Utilice el código o el cursor de Claude con habilidades de agente para andamiar, codificar y refinar los componentes de AEM guiados por las prácticas recomendadas de Adobe.</p>
                </div>
                <a href="https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Probar con habilidades de agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Invoke AEM APIs from a web app">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" title="Invocar las API de AEM desde una aplicación web" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/using-api-card.png" alt="Invocar las API de AEM desde una aplicación web"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" title="Invocar las API de AEM desde una aplicación web">Invocar las API de AEM desde una aplicación web</a>
                    </p>
                    <p class="is-size-6">Cree una aplicación web que autentique usuarios y llame a las API abiertas de AEM mediante OAuth para ofrecer acceso controlado y programático.</p>
                </div>
                <a href="https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Probar con API</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
