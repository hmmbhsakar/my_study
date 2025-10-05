# ultimate_structure.md

## Prayer
>
> सरस्वति नमस्तुभ्यं वरदे कामरूपिणि ।\
विद्यारम्भं करिष्यामि सिद्धिर्भवतु मे सदा ॥

— Agastya Saraswati Stotram

Translation
> O Sarasvati, salutations to you — giver of boons and fulfiller of desires.\
I begin my studies; may I always be granted success.

## Maths

## Computer Science

### Computer Languages

#### Programming Languages

##### General Purpose Languages

- python.md
- python_built-in_libraries.md

##### Domain Specific Languages

###### Query Languages

- SQL

###### Scripting Languages

- Bash

#### Domain Specific Language (DSL)
>
> Consist of only those DSL which are not a programming language(Turning Complete)
>
##### Markup Language

- Markdown

##### Data Serialization Language

- XML
- JSON
- YAML

##### Configuration Languages

- INI Files

##### Regular Expressions

#### Language Standards & Specifications

- ISO C (C11/C17)
- ISO C++ (C++17/C++20)
- ECMAScript (JS) standards

### Operating Systems

#### Operating Systems Fundamentals

#### Specific Operating Systems

##### Linux/Unix

##### BSDs

##### Solaris

##### Windows

##### macOs

#### Standards & Specifications

- POSIX (Portable Operating System Interface)
- UEFI
- ACPI
- FileSystems (ext4, NTFS, FAT, XFS)

### Software Engineering

#### Performance Engineering

##### Benchmarking

##### Profiling

### Human Computer Interaction

### Standards, Protocols & Architectures

#### Languages

- ISO C/C++, ECMAScript, Python Enhancement Proposals (PEPs) as language governance

#### OS

- POSIX
  - Cross-Reference:  Operating System > Standards & Specifications > POSIX

#### Networking / Internet

- RFCs (TCP, IP, UDP), HTTP/1.1, HTTP/2/3, DNS, TLS, QUIC, NFS, SMB

#### Web & Markup

- HTML, CSS, W3C APIs, ARIA, DOM

#### Data / Formats & Serialization  / Text Encodings

- Unicode (UTF-8), ISO 8601, JSON, XML, YAML, MIME

#### Databases / Query Standards

- SQL (ISO/IEC 9075), ODBC/JDBC

#### Security & Crypto

- X.509/PKI, RFCs for TLS, NIST/ISO security standards, OAuth, SAML

#### Hardware & ISA

- x86, ARM, RISC-V, PCIe, USB, SATA

#### Graphics / Compute APIs

- OpenGL, Vulkan, OpenCL, CUDA (vendor docs)

#### Cloud & Virtualization

- OCI, Container Runtime (CRIU? OCI spec), OpenStack APIs, Kubernetes API conventions

#### DevOps / CI

- POSIX shell utilities (for scripts), POSIX is directly useful for portable scripts; CI specs or best-practices docs

#### Accessibility

#### Legal/Compliance

- GDPR, PCI-DSS, accessibility standards (WCAG)

## Intelligence

### MLOps

#### Model Benchmarking

#### Model Deployment

#### Model Serving

#### Model Inference

### LLMOps/AIOps

#### GenAI Benchmarking

#### GenAI Deployment

#### GenAI Serving

#### GenAI Inference

## Data

## Tools

## Infra & Platform

### Virtualization

> A technology that enables the creation of virtual versions of computing resources, such as servers, storage, and operating systems.

#### Server Virtualization

> Partitions a physical server into multiple, isolated virtual servers, or Virtual Machines (VMs), allowing multiple operating system instances to run on a single machine.

##### Full Virtualization

> A guest OS is run on a VM without any modifications, with the hypervisor providing a complete emulation of the underlying hardware.

##### Paravirtualization

> The guest OS is modified to work with the hypervisor, allowing for more efficient resource utilization.

##### Hardware assisted virtualization

> Uses hardware features (e.g., Intel VT-x and AMD-V) to improve the performance of virtualization.

#### Network Virtualization

> Abstracts network hardware and software functionality into a single software-based administrative entity. It allows multiple virtual networks to run independently on the same physical network.

##### External Network Virtualization

> Combines multiple LANs into a single virtual network, improving efficiency for a larger network.

##### Internal Network Virtualization 

> Confines virtualization to a single system with software containers or pseudo-interfaces to emulate a physical network.

##### Software Defined Networking (SDN)

> Virtualizes the hardware that controls network traffic routing. Abstracts the network control plane from the data plane, allowing network management to be programmed centrally.

##### Network Functions Virtualizations (NFV)

> Virtualizes network hardware appliances, such as firewalls and load balancers to run on standard hardware.

#### Storage Virtualization

> Pools physical storage from multiple network storage devices and manages them as a single storage unit.

##### Host-based Virtualization

> Software installed on a server manages its local storage resources.

##### Array based Virtualization

> Virtualization features are built into the storage arrays themselves.

##### Network based Virtualization

> Uses a dedicated appliance to manage storage devices.

#### Desktop Virtualization

> Separates the desktop environment from the physical machine, allowing users to access it remotely from any device.

##### Virtual Desktop Infrastructure (VDI)

> Desktops run as VMs on a centralized server and are delivered to end-users.

##### Desktop as a Service (Daas)

> A cloud-based VDI solution managed by a third-party provider.

#### Application Virtualization

> Separates an application from the underlying OS, allowing it to run in an isolated environment or be streamed from a remote server.

##### Application Streaming

> The application code is sent to the user's device in small components as it is needed.

##### Server based virtualization

> The application runs entirely on a server, and only its user interface is sent to the client device.

#### Operating system level virtualization

> The OS kernel allows multiple isolated instances to share the same OS. This is the basis of containerization.
> Virtual Memory: Manages and dynamically allocates the physical system memory to multiple virtual machines.

#### Data virtualization

> Creates a software layer that integrates data from multiple sources into a single, virtual source for applications to access.

#### GPU Virtualization

> Allows a physical GPU to be shared across multiple virtual machines.

#### I/O Virtualization

> Allows multiple virtual machines to share physical I/O resources

## Soft Skills

## Extra

## templates

### Notes

## Creation References
> dump > directory_structure > old_ultimate_structure.md\
> [ChatGPT_hmmbhaskar](https://chatgpt.com/share/68e0cfc0-e9f0-8007-81b2-24f3c0085404)\
> dump > directory_structure > partial_ultimate_structure.md\
> subject> tools_frameworks > tentative_tools_categorization.md\
> learn.md\
> 
