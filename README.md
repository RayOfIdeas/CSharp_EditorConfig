# CSharp_EditorConfig
- The C# coding convention of RayOfIdeas
- Adopted from [Dotnet's EditorConfig](https://github.com/dotnet/docs/blob/main/.editorconfig)

# Conventions

## Naming

| Symbol                         | Style         | Example          |
| ------------------------------ | ------------- | ---------------- |
| Public fields                  | PascalCase    | `MaxSpeed`       |
| Constants                      | PascalCase    | `DefaultTimeout` |
| Methods (all)                  | PascalCase    | `GetValue()`     |
| Private/internal fields        | `_camelCase`  | `_health`        |
| Private/internal static fields | `s_camelCase` | `s_instance`     |

## Modifiers

- Omit `private` keyword — it is the default and should not be written explicitly
- Modifier order: `public, private, protected, internal, static, extern, new, virtual, abstract, sealed, override, readonly, unsafe, volatile, async`

## Types & Variables

- Prefer `var` everywhere (including built-in types)
- Use language keywords over BCL types (`int` not `Int32`, `string` not `String`)
- Avoid `this.` unless necessary

## Code Style

- Braces on their own line (Allman style) — applies to all blocks
- Always use braces, even for single-line bodies
- Prefer file-scoped namespaces (`namespace Foo;`)
- `using` directives outside the namespace, `System` directives sorted first
- Prefer expression-bodied members where possible (methods, properties, constructors, etc.)
- Prefer switch expressions over switch statements
- Prefer string interpolation over concatenation

## Null & Pattern Handling

- Prefer `?.` null propagation and `??` null coalescing
- Prefer `is null` / `is not null` over `== null`
- Prefer pattern matching over `is`-with-cast and `as`-with-null-check
- Prefer throw expressions (`x ?? throw new ...`)

## Expressions & Initializers

- Prefer object and collection initializers
- Prefer auto-properties
- Prefer inlined variable declarations (`out var x`)
- Prefer `default` over `default(T)`

## Quality

- Mark fields `readonly` when possible
- Flag unused parameters in non-public methods
- Security analyzer diagnostics treated as errors
