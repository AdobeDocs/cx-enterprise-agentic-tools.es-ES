---
title: Herramientas de agente
description: Compare servidores MCP, habilidades de agente y API para generadores y elija la herramienta original adecuada para sus flujos de trabajo empresariales de Adobe CX.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 1%

---


# Herramientas de agente

<!-- last-modified: 2026-05-08 -->

No todos los enfoques de herramientas agénticas sirven a la misma necesidad. Los servidores MCP le proporcionan acceso inmediato y en lenguaje natural a los datos de Adobe desde cualquier cliente de IA compatible, sin necesidad de codificación. Las habilidades de agente codifican la experiencia del dominio de Adobe en flujos de trabajo de agentes repetibles para que las tareas se ejecuten de forma coherente cada vez. Las API proporcionan a los desarrolladores control total de la programación para crear aplicaciones e integraciones personalizadas. Esta página explica las compensaciones para que pueda elegir el punto de partida correcto para su situación.

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

## Comparar herramientas agénticas

| | Servidores MCP | Aptitudes de agente | API para generadores |
| --- | --- | --- | --- |
| Mejor para | Usuarios de cliente de IA | Todos los usuarios | Desarrolladores |
| Requiere codificación | No | No | Sí |
| Tiempo de configuración | Minutes | Minutes | Horas a días |
| Lo que obtienes | Acceso a Adobe desde la herramienta de IA | Flujos de trabajo guiados y repetibles | Control programático completo |
| Se necesita cliente de IA | Sí | Sí | Opcional |

## ¿No estás seguro de por dónde empezar?

- Para usar la IA para interactuar con aplicaciones empresariales de Adobe CX (realizar acciones, consultar datos y permitir que la IA descubra qué hacer después a través de una conversación natural), los [servidores MCP](mcp-servers.md) son el punto de partida más flexible.
- Para que los agentes sigan de manera consistente los flujos de trabajo nativos de Adobe sin improvisar, [Habilidades de agente](agent-skills.md) codifican esa experiencia de dominio en instrucciones reutilizables.
- Para generar una aplicación enfocada que optimiza o automatiza un flujo de trabajo específico de Adobe para los usuarios, las [API para generadores](apis.md) le proporcionan control directo y programable sobre lo que sucede exactamente.

>[!BEGINTABS]

>[!TAB Servidores MCP]

Piense en los servidores MCP como un cable activo entre su herramienta de IA y Adobe. Conéctese una vez y su IA podrá consultar campañas, extraer audiencias, comprobar el estado del recorrido y mucho más. Todo en lenguaje sencillo, no se necesita código.

**Usar servidores MCP cuando:**

- Desea que los datos de Adobe estén dentro de la herramienta de IA que ya utiliza
- Está realizando análisis exploratorios o recuperación de datos ad hoc
- Desea obtener resultados rápidamente, sin dar vueltas a un proyecto

**Pruébalo:** Pídele a Claude que resuma tus recorridos activos. Extraer los tamaños de audiencia de Real-Time CDP de ChatGPT. Revise las métricas de la campaña de CJA sin abrir un tablero.

[Explorar servidores MCP](mcp-servers.md)

>[!TAB Aptitudes de agente]

Las habilidades de agente son conocimientos de dominio de Adobe, codificados como instrucciones que el agente puede seguir. En lugar de esperar que su agente descubra los pasos correctos, una habilidad le dice exactamente qué hacer. Fiable, repetible y ya ajustado para flujos de trabajo de Adobe.

**Usar aptitudes de agente cuando:**

- Desea que la misma tarea se realice de la misma manera cada vez
- Está ejecutando flujos de trabajo de producción de contenido o medios repetibles
- Desea un agente que conozca Adobe sin tener que explicarlo

**Pruébelo:** Edite en lote un conjunto de fotos para que tengan un aspecto coherente. Genere variantes sociales listas para la plataforma desde un recurso de origen. Diseñe a partir de una plantilla de Adobe Express con algunas indicaciones.

[Explorar aptitudes del agente](agent-skills.md)

>[!TAB API para generadores]

Las API son los componentes básicos. Proporcionan a los desarrolladores acceso directo y programático a los datos y las operaciones de Adobe, utilizando las mismas API que alimentan los productos propios de Adobe. Utilícelos para crear algo que se ejecute en su programación, sus términos, su pila.

**Usar API cuando:**

- Está creando una aplicación o panel personalizado
- Debe integrar los datos de Adobe en otro sistema
- Utiliza el código o cursor Claude para generar una aplicación completa
- Necesita un control completo de creación, actualización o eliminación

**Pruébelo:** Cree un panel de campañas personalizado. Automatice una canalización de datos. Genere una aplicación con Claude Code que lea y escriba en Adobe Experience Platform.

[Explorar las API para generadores](apis.md)

>[!ENDTABS]

## Usándolos juntos.

Los servidores MCP, las aptitudes de agente y las API son complementarios. Muchos flujos de trabajo combinan los tres:

- Una aptitud de agente define el flujo de trabajo y guía al agente
- Los servidores MCP proporcionan al agente acceso de lectura a los datos de Adobe en mitad del flujo de trabajo
- Las API gestionan acciones que requieren escrituras directas del sistema o lógica de aplicación personalizada
