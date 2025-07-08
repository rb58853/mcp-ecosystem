# MCP Ecosystem

<div align=center>

[![Last commit](https://img.shields.io/github/last-commit/rb58853/python-mcp.svg?style=flat)](https://github.com/rb58853/python-mcp/commits)
[![Commit activity](https://img.shields.io/github/commit-activity/m/rb58853/python-mcp)](https://github.com/rb58853/python-mcp/commits)
[![Stars](https://img.shields.io/github/stars/rb58853/python-mcp?style=flat&logo=github)](https://github.com/rb58853/python-mcp/stargazers)
[![Watchers](https://img.shields.io/github/watchers/rb58853/python-mcp?style=flat&logo=github)](https://github.com/rb58853/python-mcp)
[![Contributors](https://img.shields.io/github/contributors/rb58853/python-mcp)](https://github.com/rb58853/python-mcp/graphs/contributors)
[![Documentation](https://img.shields.io/badge/docs-modelcontextprotocol.io-blue.svg)](https://modelcontextprotocol.io)

</div>

Este repositorio actúa como un **índice centralizado** que agrupa una serie de proyectos relacionados con el **Model Context Protocol (MCP)**, un estándar abierto para conectar aplicaciones de inteligencia artificial con fuentes externas de datos y herramientas

## Table of Contents

* [Overview](#overview)
* [Repositories](#repositories)
  * [mcp-llm-client](#mcp-llm-client)
  * [mcp-oauth](#mcp-oauth)
  * [simple-mcp-server](#simple-mcp-server)
  * [template_mcp_llm_client](#template_mcp_llm_client)
  * [supabase-mcp-server](#supabase-mcp-server)
* [¿Qué es MCP?](#qué-es-mcp)

## Overview

TODO

## Repositories

### [mcp-llm-client](https://github.com/rb58853/mcp-llm-client)

### [mcp-oauth](https://github.com/rb58853/mcp-oauth)

### [simple-mcp-server](https://github.com/rb58853/)

### [template_mcp_llm_client](https://github.com/rb58853/template_mcp_llm_client)

### [supabase-mcp-server](https://github.com/rb58853/supabase-mcp-server)

---

## ¿Qué es MCP?

El **Model Context Protocol (MCP)** es un protocolo abierto y universal que estandariza la forma en que los grandes modelos de lenguaje (LLMs) y agentes de inteligencia artificial interactúan con fuentes de datos externas, herramientas y servicios en tiempo real. MCP permite que los modelos de IA accedan dinámicamente a información actualizada y ejecuten acciones externas, superando la limitación de operar de manera aislada sin conexión con sistemas externos.

### Propósito

MCP fue diseñado para resolver el problema de la fragmentación en la integración de IA con sistemas externos. Antes de MCP, cada aplicación de IA requería integraciones personalizadas para cada fuente de datos o herramienta, lo que generaba complejidad, redundancia y dificultades de mantenimiento. MCP establece un protocolo común que funciona como un "estándar universal" (similar a cómo USB unificó la conexión de dispositivos), facilitando una integración sencilla, escalable y segura entre modelos de lenguaje y recursos externos.

### Componentes y Funcionalidades

MCP define tres tipos principales de capacidades que los servidores pueden exponer a los modelos:

* **Resources (Recursos):** Puntos de acceso para obtener datos estructurados, equivalentes a endpoints GET, que permiten cargar información relevante en el contexto del modelo, por ejemplo, bases de datos, documentos, APIs.

* **Tools (Herramientas):** Funciones o acciones que el modelo puede invocar para ejecutar código o realizar efectos secundarios, similares a endpoints POST. Por ejemplo, enviar correos, ejecutar consultas, activar procesos.

* **Prompts (Plantillas):** Plantillas reutilizables que definen patrones de interacción con el modelo, estandarizando cómo se formulan y procesan las solicitudes.

### Arquitectura

MCP sigue una arquitectura cliente-servidor compuesta por:

* **Hosts MCP:** Aplicaciones o interfaces que utilizan modelos de IA y desean acceder a datos o funcionalidades externas.

* **Clientes MCP:** Clientes que mantienen conexiones individuales con servidores MCP para solicitar y recibir información.

* **Servidores MCP:** Servicios que exponen recursos, herramientas y prompts a través del protocolo MCP.

* **Fuentes de Datos Locales y Servicios Remotos:** Bases de datos, archivos, APIs o servicios externos que los servidores MCP pueden consultar o manipular.

Esta arquitectura transforma el problema de integración de un esquema M×N (múltiples clientes por múltiples servidores) a una solución M+N, al introducir una capa de abstracción común que facilita la interoperabilidad.

### Beneficios Clave

* **Integración simplificada:** Reduce la necesidad de desarrollos personalizados para cada combinación de modelo y fuente de datos.

* **Interoperabilidad:** Permite que cualquier cliente MCP funcione con cualquier servidor MCP compatible.

* **Acceso en tiempo real:** Facilita que los modelos consulten datos actualizados y relevantes al momento de la interacción.

* **Escalabilidad y mantenimiento:** Al estandarizar el protocolo, se facilita la expansión y actualización de sistemas sin afectar la compatibilidad.

* **Seguridad y control:** Permite que las organizaciones mantengan control sobre sus datos sensibles, integrando IA local con sistemas empresariales de forma segura.
