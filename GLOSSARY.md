# Glossary of WGSL Importing terms

- WESL: The extended WGSL language, and is pronounced like "weasel". Stands for WGSL Extended Shading Language
- Importable item
  - Structs
  - Functions 
  - Type aliases
  - [Const declarations, override declarations](https://www.w3.org/TR/WGSL/#value-decls)
  - [Var declarations](https://www.w3.org/TR/WGSL/#var-decls) 
- Module: A single WESL file
- Root Module: A WESL module from which compilation starts. A single project can have many root modules.
- Module Path: Hierarchical address of a module file or partial path, akin to a filesystem path
- Side effects: WGSL code that can affect other modules when imported
  - Things that are specified when [creating a WGSL pipeline](https://developer.mozilla.org/en-US/docs/Web/API/GPUDevice/createRenderPipeline#fragment_object_structure)
    - Shader entry-points
    - Pipeline-overridable constants
    - Global variables, including bindings
  - [Directives](https://www.w3.org/TR/WGSL/#directives): Generated WGSL code must agree on a set of directives
  - (Maybe `const_assert`?)
- Package: A publishable body of WESL code containing multiple files. Akin to a JavaScript npm package or a Rust crate. 
- Package Root: The root directory of WESL files
- Visibility: Whether a importable item is visible to
  - other modules
  - other packages
