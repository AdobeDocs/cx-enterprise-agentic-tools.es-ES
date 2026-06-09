---
title: Aptitudes de agente
description: Flujos de trabajo e instrucciones seleccionados por Adobe que guían a los agentes de IA a través de las tareas de CX Enterprise de forma coherente.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: 8f499ad7baf1b5d08dfac90511d0c76e8372c08b
workflow-type: tm+mt
source-wordcount: '440'
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
