# Python MCP

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/pypi/v/mcp-sys-bridge?color=%2334D058&label=Version)](https://pypi.org/project/mcp-sys-bridge)
[![Last commit](https://img.shields.io/github/last-commit/rb58853/python-mcp.svg?style=flat)](https://github.com/rb58853/python-mcp/commits)
[![Commit activity](https://img.shields.io/github/commit-activity/m/rb58853/python-mcp)](https://github.com/rb58853/python-mcp/commits)
[![Stars](https://img.shields.io/github/stars/rb58853/python-mcp?style=flat&logo=github)](https://github.com/rb58853/python-mcp/stargazers)
[![Forks](https://img.shields.io/github/forks/rb58853/python-mcp?style=flat&logo=github)](https://github.com/rb58853/python-mcp/network/members)
[![Watchers](https://img.shields.io/github/watchers/rb58853/python-mcp?style=flat&logo=github)](https://github.com/rb58853/python-mcp)
[![Contributors](https://img.shields.io/github/contributors/rb58853/python-mcp)](https://github.com/rb58853/python-mcp/graphs/contributors)

A python implementation of the **Model Context Protocol (MCP)**....

---

## Table of Contents

* [Overview](#overview)
* [Repositories](#repositories)
  * [Simple python mcp server](#simple-python-mcp-server)
* [License](#license)

---

# MCP Ecosystem - Repositorios y Visión General

Este repositorio actúa como un **índice centralizado** que agrupa una serie de proyectos relacionados con el **Model Context Protocol (MCP)**, un estándar abierto para conectar aplicaciones de inteligencia artificial con fuentes externas de datos y herramientas.

---

## ¿Qué es MCP?

El **Model Context Protocol (MCP)** es un protocolo abierto diseñado para estandarizar la forma en que las aplicaciones de IA, como chatbots, asistentes en IDEs o agentes personalizados, se conectan con sistemas externos, bases de datos y APIs. MCP funciona como un "USB para integraciones de IA", simplificando la conexión entre múltiples modelos de lenguaje y diversas herramientas o fuentes de datos.

### Objetivos y Beneficios

- **Unificación de integraciones:** Evita la necesidad de construir integraciones M×N (modelos × herramientas) al transformar el problema en M+N, con MCP clientes (en las aplicaciones) y MCP servidores (en las fuentes de datos).
- **Arquitectura cliente-servidor:** Los hosts (aplicaciones de usuario) se conectan a servidores MCP que exponen funciones, recursos y prompts mediante un protocolo estándar.
- **Flexibilidad y escalabilidad:** Facilita cambiar entre proveedores de modelos y ampliar las capacidades sin rehacer integraciones.
- **Seguridad y estandarización:** Usa JSON-RPC 2.0 para la comunicación y soporta transportes como STDIO y HTTP+SSE.

### Componentes Principales

| Componente       | Descripción                                                                                  |
|------------------|----------------------------------------------------------------------------------------------|
| **Host**         | Aplicación que interactúa con el usuario y usa MCP para acceder a datos (ej. Claude Desktop) |
| **Cliente MCP**  | Módulo dentro del host que gestiona la conexión con un servidor MCP específico               |
| **Servidor MCP** | Programa externo que expone herramientas, recursos y prompts para el modelo                  |
| **Transporte**   | Canales de comunicación (STDIO local o HTTP+SSE remoto)                                     |

### Casos de Uso

- Acceso a repositorios de código
- Consultas a bases de datos
- Integración con APIs externas (clima, gestión de tareas, etc.)
- Automatización y asistentes inteligentes en entornos de desarrollo

---

## Repositorios Incluidos

| Repositorio                         | Descripción breve                                           |
|-----------------------------------|-------------------------------------------------------------|
| [simple-mcp-server](https://github.com/rb58853/simple-mcp-server)       | Servidor MCP básico para pruebas y desarrollo rápido         |
| [mcp-oauth](https://github.com/rb58853/mcp-oauth)                       | Implementación de autenticación OAuth para MCP               |
| [mcp-llm-client](https://github.com/rb58853/mcp-llm-client)             | Cliente MCP para integración con modelos de lenguaje         |
| [template_mcp_llm_client](https://github.com/rb58853/template_mcp_llm_client) | Plantilla para construir clientes MCP personalizados          |
| [supabase-mcp-server](https://github.com/rb58853/supabase-mcp-server)   | Servidor MCP para integración con bases de datos Supabase    |

---

