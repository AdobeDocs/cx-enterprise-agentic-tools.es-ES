---
title: Aptitudes de agente
description: Flujos de trabajo e instrucciones seleccionados por Adobe que guían a los agentes de IA a través de las tareas de CX Enterprise de forma coherente.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: f7ace53bd5988b5902659c89c6da16448398e0c0
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---


# Aptitudes de agente

<!-- last-modified: 2026-05-19 -->

![Aptitudes de agente para Adobe CX Enterprise](../assets/hero-agent-skills.png)

Las habilidades de agente son flujos de trabajo depurados por Adobe que proporcionan a los agentes de IA instrucciones paso a paso para completar de forma fiable las tareas empresariales de Adobe CX. Cada habilidad del agente codifica la experiencia del dominio y las prácticas recomendadas para que los agentes produzcan resultados coherentes y validados sin necesidad de improvisar. Las habilidades de agente tienen sentido cuando desea un comportamiento repetible y guiado en todas las conversaciones, especialmente para tareas que, de lo contrario, requerirían una solicitud detallada cada vez. Se complementan con los servidores MCP y las API: las habilidades del agente definen cómo funciona un agente; los servidores MCP y las API proporcionan el acceso subyacente.

## Aptitudes de agente empresarial de Adobe CX

Seleccione un área de capacidades a continuación para explorar las habilidades de ese flujo de trabajo.

>[!BEGINTABS]

>[!TAB Adobe Experience Manager]

Aptitudes de agente para el desarrollo, contenido, diseño y administración de proyectos de Experience Manager en AEM as a Cloud Service, Edge Delivery Services y AEM 6.5 LTS.

[Ver aptitudes del agente](https://github.com/adobe/skills/tree/main/plugins/aem)

>[!TAB Adobe Analytics]

Aptitudes de agente para flujos de trabajo de monitorización de KPI, análisis de funnel y creación de informes ejecutivos en Adobe Analytics.

[Ver aptitudes del agente](https://github.com/adobe/skills/tree/main/plugins/adobe-analytics)

>[!TAB Customer Journey Analytics]

Habilidades del agente para la comparación de rendimiento, análisis de dimensión y creación de espacios de trabajo en Customer Journey Analytics.

[Ver aptitudes del agente](https://github.com/adobe/skills/tree/main/plugins/adobe-cja)

>[!TAB Adobe App Builder]

Aptitudes de agente para andamiaje, pruebas e implementación de aplicaciones personalizadas con Adobe App Builder.

[Ver aptitudes del agente](https://github.com/adobe/skills/tree/main/plugins/app-builder)

>[!TAB Creative Cloud]

Habilidades del agente para la edición fotográfica por lotes, diseño a partir de plantillas, edición de vídeo y variantes de medios sociales con Creative Cloud.

[Ver aptitudes del agente](https://github.com/adobe/skills/tree/main/plugins/creative-cloud)

>[!ENDTABS]

## Agregar aptitudes de agente

![Funcionamiento de las aptitudes del agente](../assets/hero-connect-agent-skills.gif)

Una aptitud de agente es un conjunto de instrucciones que indica a un agente de IA cómo completar una tarea mediante las herramientas agénticas de Adobe. Cuando un agente carga una habilidad, sigue ese flujo de trabajo en lugar de improvisar.

### Instalar aptitudes de agente

Las aptitudes de agente se instalan en función del cliente de IA que utilice. Algunos clientes admiten la instalación directa desde la línea de comandos:

- **Código Claude**: `/plugin install adobe/skills`
- **Entornos de nodo**: `npx skills add adobe/skills`
- **CLI de GitHub**: `gh upskill adobe/skills`

Otros clientes requieren que descargue y agregue los archivos de aptitudes directamente a su cliente de IA. Consulte el archivo LÉAME de aptitudes de Adobe [en GitHub](https://github.com/adobe/skills#installation) para obtener instrucciones de instalación completas del cliente.

### Búsqueda de aptitudes de agente

Examine la lista completa de aptitudes disponibles en el [repositorio de GitHub de aptitudes de Adobe](https://github.com/adobe/skills). Cada habilidad del agente incluye un archivo de `SKILL.md` con instrucciones, referencias y ejemplos detallados.

Después de instalar o agregar el paquete `adobe/skills`, algunos clientes de IA le permiten enumerar todas las habilidades disponibles directamente:

- **Código Claude**: `claude /plugin list`
- **Entornos de nodo**: `npx skills list`
- **CLI de GitHub**: `gh upskill list`

## Aptitudes de agente en acción

Las habilidades de agente ponen a los expertos en dominios de Adobe a trabajar dentro de su cliente de IA, por lo que los agentes siguen flujos de trabajo comprobados en lugar de improvisar. Cada uno de los tutoriales siguientes muestra una tarea empresarial específica que se ha completado de forma fiable, guiada por las prácticas recomendadas de Adobe desde el principio hasta el final.

<!--
CARDS

* https://experienceleague.adobe.com/es/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
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
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
