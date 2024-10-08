![banner](https://raw.githubusercontent.com/zuspec/zuspec.github.io/main/imgs/ZuspecProjectMap.png)

# Zuspec - An Action Relation Level Modeling Framework
Zuspec provides a set of tools for working with action relation level
(ARL) models, primarily those described using the 
[Accellera Portable Test and Stimulus (PSS)](https://www.accellera.org/downloads/standards/portable-stimulus) language. ARL models are used today to
specify system-level tests for digital designs, but they lend themselves
to many more applications as well. Zuspec has a very modular design to support
rapidly exploring new applications for this modeling methodology.

## Project Components

The bulk of Zuspec components are implemented in C++, with functionality
available via both a C++ API and a Python API. Components are designed
such that they can be integrated via Python, but interact at full speed
via the C++ implementation.

### Applications
Applications are how most users will experience Zuspec. Applications 
connect one or more Zuspec components, together with some integration
code, to address a specific need. 
- Zuspec -- Support for code generation
- Zuspec-SV -- Integration support for SystemVerilog testbench environments
- Zuspec-Py -- Integration support for running ARL models in Python
- langserver -- [VSCode](https://code.visualstudio.com/) language server

### Front-Ends
Front-ends process and input description (such as Accellera PSS), typically
with the goal of populating Zuspec's ARL data model for further 
processing and evaluation
- Parser -- ANTLR-based parser and AST for Accellera PSS (with language extensions)
- FE-Parser -- AST to ARL datamodel converter
- Python Dataclasses -- Python-based DSL for capturing ARL descriptions. Mostly used for testing

### Core Data Model and Evaluation
ARL models are typically primarily declarative descriptions. In other words, they
are heavily constraint-based. Evaluation tools process the data model to 
execute it and to optimize it.

arl-dm -- Core data model capturing ARL modeling semantics
arl-eval -- Core evaluator, enabling interpretive evaluation of an ARL model
vsc-dm -- External data model for constrained-random descriptions
vsc-solvers -- Bundle of constraint solvers used by the evaluator

### Back-Ends
Backends integrate Zuspec evaluation into specific environments or directly
produce executable representations of ARL models.

- be-sv -- SystemVerilog integration and code generators
- be-sw -- Code generators for C and C++ outputs
- be-py -- Python integration for evaluating ARL models in Python
- be-pss -- Emit ARL as lowered Accellera PSS


## Project Status
Zuspec is under active development, but not yet ready for use. Watch this 
space for updates on the project's status.

## Build Status
- **zuspec-arl-dm** - ![zuspec-arl-dm](https://github.com/zuspec/zuspec-arl-dm/actions/workflows/ci.yml/badge.svg)
- **zuspec-arl-eval** - ![zuspec-arl-eval](https://github.com/zuspec/zuspec-arl-eval/actions/workflows/ci.yml/badge.svg)
- **zuspec-be-sw** - ![zuspec-be-sw](https://github.com/zuspec/zuspec-be-sw/actions/workflows/ci.yml/badge.svg)
- **zuspec-cli** - ![zuspec-cli](https://github.com/zuspec/zuspec-cli/actions/workflows/ci.yml/badge.svg)
- **zuspec-fe-parser** - ![zuspec-fe-parser](https://github.com/zuspec/zuspec-fe-parser/actions/workflows/ci.yml/badge.svg)
- **zuspec-parser** - ![zuspec-parser](https://github.com/zuspec/zuspec-parser/actions/workflows/ci.yml/badge.svg)
- **zuspec-py** - ![zuspec-apy](https://github.com/zuspec/zuspec-py/actions/workflows/ci.yml/badge.svg)
- **zuspec-sv** - ![zuspec-sv](https://github.com/zuspec/zuspec-sv/actions/workflows/ci.yml/badge.svg)

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
