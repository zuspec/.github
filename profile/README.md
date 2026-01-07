# Zuspec: A Multi-Abstraction, Multi-Platform Hardware Modeling Tool

```mermaid
graph TD
    A["User Code(zuspec.dataclasses)"] --> B{"Target"}
    B -->|Pure Python| C["Executable Python"]
    B -->|Retargetable| D["Intermediate Representation (IR)"]
    D --> E["Transform & Manipulate"]
    E --> Ep["Implement"]
    Ep --> F["SystemVerilog Behavioral Model"]
    Ep --> G["SystemVerilog RTL"]
    Ep --> H["Fast C/C++ Model"]
    Ep --> I["Static/Formal Model"]
    
    style A fill:#5dade2,stroke:#333,stroke-width:2px,color:#000
    style C fill:#58d68d,stroke:#333,stroke-width:2px,color:#000
    style D fill:#f39c12,stroke:#333,stroke-width:2px,color:#000
    style E fill:#f39c12,stroke:#333,stroke-width:2px,color:#000
    style F fill:#bb8fce,stroke:#333,stroke-width:2px,color:#000
    style G fill:#bb8fce,stroke:#333,stroke-width:2px,color:#000
    style H fill:#bb8fce,stroke:#333,stroke-width:2px,color:#000
    style I fill:#bb8fce,stroke:#333,stroke-width:2px,color:#000
```

A significant portion of the silicon design process is spent making and evaluating
models. We'd like to model the intended behavior of the design early on and 
test our assumptions by executing it and running symbolic/formal checks against it.
While the RTL designers are busy, the DV engineers would like to get a head start
on writing tests, leveraging the functional model. And, we'd like the ability to
take the programming sequences that the DV engineers have created and easily 
leverage those for emulation and once silicon comes back. 

It's possible to get some or all of these individual benefits with existing 
languages or class libraries. But, these modeling tools and techniques
are siloed, leading to significant re-work and increasing the risk of introducing
inconsistencies between the models. 

Zuspec, a portmanteau of Zusammen (*together* in German) and Specification, seeks to
unify hardware modeling under a Python-based framework. 

## Project Status
Zuspec is under active development, but not yet ready for use. Watch this 
space for updates on the project's status.

## Build Status
- **zuspec** - ![zuspec](https://github.com/zuspec/zuspec/actions/workflows/ci.yml/badge.svg)
- **zuspec-dataclasses** - ![zuspec-dataclasses](https://github.com/zuspec/zuspec-dataclasses/actions/workflows/ci.yml/badge.svg)
- **zuspec-be-sv** - ![zuspec-be-sv](https://github.com/zuspec/zuspec-be-sv/actions/workflows/ci.yml/badge.svg)
- **zuspec-be-sw** - ![zuspec-be-sv](https://github.com/zuspec/zuspec-be-sw/actions/workflows/ci.yml/badge.svg)

