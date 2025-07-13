# MCP Ecosystem

<div align=center>

[![Stars](https://img.shields.io/github/stars/rb58853/mcp-ecosystem?style=flat&logo=github)](https://github.com/rb58853/mcp-ecosystem/stargazers)
[![Watchers](https://img.shields.io/github/watchers/rb58853/mcp-ecosystem?style=flat&logo=github)](https://github.com/rb58853/mcp-ecosystem)
[![Contributors](https://img.shields.io/github/contributors/rb58853/mcp-ecosystem)](https://github.com/rb58853/mcp-ecosystem/graphs/contributors)
[![Documentation](https://img.shields.io/badge/docs-modelcontextprotocol.io-blue.svg)](https://modelcontextprotocol.io)

</div>

This repository acts as a **centralized index** that groups together a series of projects related to the **Model Context Protocol (MCP)**, an open standard for connecting artificial intelligence applications with external data sources and tools.

## Table of Contents

* [Overview](#overview)
* [Repositories](#repositories)
  * [mcp-llm-client](#mcp-llm-client)
  * [mcp-oauth](#mcp-oauth)
  * [supabase-mcp-server](#supabase-mcp-server)
  * [simple-mcp-server](#simple-mcp-server)
  * [template_mcp_llm_client](#template_mcp_llm_client)
* [What is MCP?](#what-is-mcp)

## Overview

The **MCP Ecosystem** serves as a centralized hub for projects built around the Model Context Protocol (MCP), an open standard designed to seamlessly connect artificial intelligence applications with external data sources, tools, and services. This repository consolidates a diverse set of tools, servers, and client libraries that implement or extend MCP, making it easier for developers and organizations to integrate AI models with real-world data and functionalities.

By providing reference implementations, modular components, and standardized interfaces, the MCP Ecosystem accelerates the adoption of MCP in both research and production environments. Whether you are building custom AI agents, deploying secure MCP servers, or experimenting with new integration protocols, this collection offers practical resources to streamline development and foster interoperability.

Key features of the MCP Ecosystem include:

* A curated set of repositories covering client libraries, authentication systems, server implementations, and integration templates.
* Emphasis on security, extensibility, and adherence to MCP standards.
* Comprehensive documentation and active community support to facilitate onboarding and collaboration.

The MCP Ecosystem is ideal for anyone seeking to bridge the gap between advanced AI models and the complex landscape of external data and services, enabling scalable, secure, and future-proof integrations.

## Repositories

### [mcp-llm-client](https://github.com/rb58853/mcp-llm-client)

Python client, based on [`mcp[cli]`](https://github.com/modelcontextprotocol/python-sdk), for connecting to MCP servers through multiple protocols, specifically designed to work with integrated language models.

This package provides a Python interface to connect to MCP servers in an easy, intuitive, and configurable way. It offers a modular architecture that allows for easy extension of new transfer protocols and language models. Currently includes support for HTTPStream and GPT-4 mini, with expansion capability for more options in the future.

### [mcp-oauth](https://github.com/rb58853/mcp-oauth)

This repository constitutes an OAuth system in Python that implements both server and client, following an OAuth authentication flow that integrates in a standard way with `FastMCP`. As a base, it uses the OAuth system from the official repository [modelcontextprotocol/python-sdk](https://github.com/modelcontextprotocol/python-sdk/tree/main/examples).

This project represents a simple and extensible OAuth system in Python, integrated as much as possible with MCP standards and practices. Its goal is to facilitate the use of the OAuth system for MCP. It is integrated with the official MCP Python SDK (`"mcp[cli]"`), following the source code standard that provides the basis for the entire authorization system used and controlled by `FastMCP`.

Both an OAuth server and client are implemented, respecting the most common standards to maintain standardization. It is important to highlight that the OAuth server standard in the MCP context is still poorly defined and with scarce documentation, so the greatest possible standardization has been sought both in the server and client code.

This repository starts from the Antropic example in the [official repository](https://github.com/modelcontextprotocol/python-sdk/tree/main/examples), modifying and restructuring the code to achieve optimal organization, facilitating practical and easy use when installing this repository as a pip package.

### [supabase-mcp-server](https://github.com/rb58853/supabase-mcp-server)

This project constitutes an extension of the [supabase-mcp-server](https://github.com/alexander-zuev/supabase-mcp-server) repository. [Query MCP](https://github.com/alexander-zuev/supabase-mcp-server) is an open-source MCP server that enables integrated development environments (IDEs) to safely execute SQL queries, manage schema changes, access the Supabase Management API, and use the Auth Admin SDK—all with built-in security controls.

The newly incorporated features include:

* An authentication and authorization system based on OAuth2.
* Implementation of the Streamable HTTP transport protocol.
* Compatibility with self-hosted Supabase servers deployed via Docker, using the official [docker-compose](https://github.com/supabase/supabase/tree/master/docker) configuration provided by Supabase.

These enhancements expand the original capabilities of the MCP server, enabling more secure and flexible integration with modern development environments and custom deployments.

### [simple-mcp-server](https://github.com/rb58853/simple-mcp-server)

A Python implementation of the **Model Context Protocol (MCP)** server with `fastmcp` and `fastapi`.

This repository is based on the official MCP Python SDK repository, with the objective of creating an MCP server in Python using FastMCP. The project incorporates the following basic functionalities:

* To facilitate understanding and working with the Model Context Protocol (MCP), from the fundamentals and in an accessible manner
* To provide a testing platform for MCP clients
* To integrate the server with FastAPI and offer it as a streamable HTTP service, maintaining a clear separation between the service and the client

The project focuses on the implementation of a simple MCP server that is served through FastAPI with httpstream. This approach represents the recommended methodology for creating MCP servers. To explore other implementation forms and server services, it is recommended to consult [the official documentation](https://github.com/modelcontextprotocol/python-sdk).

### [template_mcp_llm_client](https://github.com/rb58853/template_mcp_llm_client)

Reference repository for evaluating and testing the [`mcp-llm-client`](https://github.com/rb58853/mcp-llm-client) package. This template enables quick verification of client integration and functionality, as well as testing your own or third-party MCP servers. For detailed information about the MCP client with LLM integration, please refer to the [official repository](https://github.com/rb58853/mcp-llm-client).

This project provides a minimal structure to test the [`mcp-llm-client`](https://github.com/rb58853/mcp-llm-client) package and associated MCP servers. It allows for agile and reproducible validation of features, serving as a starting point for further development or additional integrations.


## What is MCP?

The **Model Context Protocol (MCP)** is an open and universal protocol that standardizes how large language models (LLMs) and artificial intelligence agents interact with external data sources, tools, and services in real time. MCP enables AI models to dynamically access up-to-date information and execute external actions, overcoming the limitation of operating in isolation without connection to external systems.

### Purpose

MCP was designed to solve the problem of fragmentation in AI integration with external systems. Before MCP, each AI application required custom integrations for each data source or tool, resulting in complexity, redundancy, and maintenance difficulties. MCP establishes a common protocol that works as a "universal standard" (similar to how USB unified device connections), enabling simple, scalable, and secure integration between language models and external resources.

### Components and Features

MCP defines three main types of capabilities that servers can expose to models:

* **Resources:** Access points for obtaining structured data, equivalent to GET endpoints, allowing relevant information to be loaded into the model's context, e.g., databases, documents, APIs.

* **Tools:** Functions or actions that the model can invoke to execute code or perform side effects, similar to POST endpoints. For example, sending emails, running queries, triggering processes.

* **Prompts:** Reusable templates that define interaction patterns with the model, standardizing how requests are formulated and processed.

### Architecture

MCP follows a client-server architecture composed of:

* **MCP Hosts:** Applications or interfaces that use AI models and want to access external data or functionalities.

* **MCP Clients:** Clients that maintain individual connections with MCP servers to request and receive information.

* **MCP Servers:** Services that expose resources, tools, and prompts through the MCP protocol.

* **Local Data Sources and Remote Services:** Databases, files, APIs, or external services that MCP servers can query or manipulate.

This architecture transforms the integration problem from an M×N scheme (multiple clients for multiple servers) to an M+N solution, by introducing a common abstraction layer that facilitates interoperability.

### Key Benefits

* **Simplified integration:** Reduces the need for custom development for each combination of model and data source.

* **Interoperability:** Allows any MCP client to work with any compatible MCP server.

* **Real-time access:** Enables models to query up-to-date and relevant data at the moment of interaction.

* **Scalability and maintenance:** By standardizing the protocol, it facilitates the expansion and updating of systems without affecting compatibility.

* **Security and control:** Allows organizations to maintain control over their sensitive data, integrating local AI with enterprise systems securely.
