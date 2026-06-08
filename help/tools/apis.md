---
title: API para generadores
description: Cree aplicaciones e integraciones personalizadas con las API de Adobe CX Enterprise.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 3%

---


# API para generadores

<!-- last-modified: 2026-06-02 -->

![API de Adobe CX para empresas](../assets/hero-apis.png)

Las API de Adobe CX Enterprise proporcionan a los desarrolladores y a las herramientas agénticas de codificación asistida por IA acceso directo a los datos y flujos de trabajo de Adobe. Utilícelos para crear aplicaciones personalizadas, automatizar integraciones e incrustar las funcionalidades de Adobe en sus propios sistemas. Las API son la elección correcta cuando necesita un control programático completo de una integración de sistema o cuando está creando una aplicación sobre los datos de Adobe. Para obtener acceso conversacional a los flujos de trabajo de Adobe impulsado por el agente, consulte [servidores MCP](mcp-servers.md).

## API de Adobe CX para empresas

Las API de Adobe CX Enterprise exponen los datos y las operaciones principales que alimentan productos como Adobe Experience Platform, Journey Optimizer y Customer Journey Analytics. Cada API sigue un diseño centrado en la API, que proporciona a los desarrolladores y a las herramientas agénticas de codificación asistida por IA acceso directo y programable a las mismas funciones que utiliza Adobe internamente. Utilícelos para crear aplicaciones personalizadas, automatizar flujos de trabajo e integrar datos de Adobe en sus propios sistemas.

<!--
CARDS

* https://developer.adobe.com/audience-manager/
  {title = Audience Manager}
  {description = Audience management and activation workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aam-card.png}

* https://developer.adobe.com/client-sdks/home/
  {title = Client SDKs}
  {description = Mobile SDKs, edge SDKs, and in-app messaging.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/cja-apis/docs/
  {title = Customer Journey Analytics}
  {description = Analytics data access, reporting, and CJA insights workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cja-card.png}

* https://developer.adobe.com/data-collection-apis/docs/
  {title = Data Collection}
  {description = Edge Network data ingestion, real-time event collection, and streaming data delivery.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/developer-console/docs/guides/
  {title = Developer Console}
  {description = API project setup, authentication, and credential management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/events/docs/
  {title = Events}
  {description = Event-driven integrations, webhooks, and automation triggers.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://experienceleague.adobe.com/en/docs/experience-platform/privacy/home
  {title = Privacy}
  {description = Privacy workflows, data governance, and data subject requests.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/experience-platform-apis/
  {title = Adobe Experience Platform}
  {description = CRUD operations for datasets, schemas, profiles, identities, queries, and segmentation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/journey-optimizer-apis/
  {title = Adobe Journey Optimizer}
  {description = Journey orchestration, campaign management, content templates, and offer decisioning.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-ajo-card.png}

* https://developer.adobe.com/analytics-apis/docs/2.0/
  {title = Adobe Analytics}
  {description = Reporting, data feeds, calculated metrics, and segment management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions
  {title = AEM as a Cloud Service}
  {description = Content, asset, and workflow management APIs for Adobe Experience Manager.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aem-card.png}

* https://developer.adobe.com/commerce/webapi/
  {title = Adobe Commerce}
  {description = REST and GraphQL APIs for catalog, cart, orders, customers, and promotions.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-commerce-card.png}

* https://developer.adobe.com/umapi/
  {title = User Management}
  {description = User management, identity administration, and enterprise account automation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}
-->

## API para generadores y servidores MCP

Utilice las API cuando necesite un control total sobre la integración del sistema o esté creando una aplicación personalizada. Utilice los servidores MCP cuando desee que un agente de IA trabaje directamente con flujos de trabajo de Adobe.

| | API | Servidores MCP |
| --- | --- | --- |
| Integración directa del sistema | Sí | A veces |
| Orquestación compatible con agentes | Limitado | Sí |
| Acceso a datos sin procesar | Sí | Generalmente abstracto |
| Desarrollo de aplicaciones personalizadas | Caso de uso principal | Secundario |
| Flujos de trabajo asistidos por IA | Admitido | Caso de uso principal |

## Introducción a las API para generadores

![Un IDE que se conecta a las API de Adobe CX Enterprise](../assets/hero-connect-apis.gif)

Las API de Adobe CX Enterprise requieren dos cosas antes de poder crearse: credenciales autenticadas de Adobe Developer Console y documentación de API agregada al proyecto para que el agente de codificación pueda trabajar con las API de Adobe de forma fiable.

### Configuración de credenciales de API en Adobe Developer Console

Todo el acceso a la API de Adobe CX Enterprise se administra mediante [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/). Cree un proyecto, añada las API que necesita la aplicación y genere credenciales.

1. Inicie sesión y [cree un proyecto](https://developer.adobe.com/developer-console/docs/guides/projects/) en Adobe Developer Console.
2. [Agregue la API](https://developer.adobe.com/developer-console/docs/guides/services/) para la aplicación Adobe CX Enterprise que necesita.
3. Elija un [tipo de autenticación](https://developer.adobe.com/developer-console/docs/guides/authentication/). Utilice **OAuth Server-to-Server** para flujos de trabajo automatizados o **OAuth Web App** para aplicaciones orientadas al usuario.
4. Genere sus credenciales. Tenga en cuenta el ID de cliente, el secreto de cliente y el extremo de token para su uso en la aplicación.

La mayoría de las API empresariales de Adobe CX requieren licencias de aplicación. Si una API no está disponible en el proyecto de Developer Console, póngase en contacto con su representante de Adobe.

### Añada el contexto de la API de Adobe a su proyecto

Los agentes de codificación de IA pueden descubrir y utilizar las API de Adobe de forma fiable al añadir el material de referencia adecuado al proyecto. Esto funciona para cualquier API de Adobe CX Enterprise que publique una especificación de OpenAPI.

**1. Buscar la especificación de API**

Examine las [API de Adobe CX Enterprise](#adobe-cx-enterprise-apis) enumeradas anteriormente o vaya directamente al [catálogo de API de Adobe Developer](https://developer.adobe.com/apis).

**2. Descargar la especificación de OpenAPI**

Cree un directorio `/specs` en su proyecto. Descargue OpenAPI YAML desde la página Referencias de la API en [developer.adobe.com](https://developer.adobe.com/apis) y guárdela allí. Agregue un(a) `README.md` registrando la URL de origen y la fecha de descarga.

```
/specs/README.md
/specs/aem-assets.openapi.yaml
```

>[!TIP]
>Una captura de pantalla protegida proporciona a su agente de codificación un comportamiento estable y reproducible, y hace que los cambios de API sean visibles en su historial de Git.

**3. Generar un índice de API**

Pegue este mensaje en su agente de codificación y reemplace `<API-SPEC-FILE>` por su nombre de archivo:

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and generate /docs/<API-SPEC-FILE>.api.md.

Create a concise API index for AI coding agents. For each operation include: operationId, HTTP method, path, purpose, authentication requirements, required inputs, response shape, common error responses, pagination behavior, asynchronous behavior, and deprecation status.

Do not invent endpoints, parameters, request bodies, response fields, or behavior not present in the OpenAPI specification.
```

**4. Generar instrucciones del agente**

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and /docs/<API-SPEC-FILE>.api.md.

Generate AGENTS.md. Instructions should:
- Treat the OpenAPI specification as the source of truth.
- Use the API index as a navigation guide.
- Never invent endpoints, parameters, response fields, or status codes.
- Prefer documented operationIds.
- Avoid deprecated or experimental APIs unless explicitly requested.
- Follow authentication requirements defined in the specification.
- Use the local OpenAPI snapshot for implementation decisions.
```

**5. Verificar**

Solicite al agente de codificación que complete una tarea sencilla utilizando únicamente los archivos generados:

```
Write a function that takes an AEM asset ID and returns the asset title and description. Use only /specs/aem-assets.openapi.yaml and /docs/aem-assets.api.md.
```

Si el agente lo completa correctamente sin inventar el comportamiento, la configuración se completa.

**Estructura de proyecto recomendada**

```
project/
├── specs/
│   ├── README.md
│   └── aem-assets.openapi.yaml
├── docs/
│   └── aem-assets.api.md
└── AGENTS.md
```

**Manteniendo las especificaciones actualizadas**

Cuando Adobe publique una nueva versión de la API: descargue una instantánea nueva en `/specs`, actualice la fecha en `README.md` y vuelva a generar el índice y `AGENTS.md`.
