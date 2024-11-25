---
weight: 1
---

# System Design

Vex employs a deliberately streamlined architecture that prioritizes simplicity and performance. Unlike many traditional language implementations that utilize Abstract Syntax Trees (AST), Vex takes a more direct approach with just two main components:

- Lexer: Handles token generation
- Parser: Processes tokens and executes commands directly

This design decision was made to minimize processing overhead while maintaining functionality for text processing operations.

# Design Rationale

## Why No AST?

The decision to omit an AST was deliberate, based on several key factors:

- **Simplified Syntax:** Vex's domain-specific nature means its syntax is straightforward enough that an AST would add unnecessary complexity
- **Performance Focus:** Direct token processing reduces memory allocation and garbage collection overhead
- **Streaming Capability:** The simplified architecture allows for efficient streaming of large text files
- **Reduced Complexity:** Fewer components mean fewer potential points of failure

## Processing Pipeline

The text processing pipeline follows a simple flow:

```shell
Input Text → Lexer → Token Stream → Parser → Output
```

This streamlined approach enables:

- Minimal memory footprint
- Direct processing of tokens
- Efficient handling of large files

# Performance Considerations

The simplified architecture brings several performance benefits:

1. Memory Efficiency

    - No tree structure allocation/deallocation
    - Reduced garbage collection pressure
    - Lower memory footprint

2. Processing Speed

   - Direct token processing without tree traversal
   - Streamlined execution path
   - Fewer object allocations

3. Scalability

   - Efficient handling of large files
   - Linear processing complexity
   - Predictable resource usage

# Error Handling

Error handling is implemented at both lexer and parser levels:

- Lexer: Handles character-level and token-level errors
- Parser: Manages syntax and semantic errors
- Runtime: Handles execution and I/O errors

# Future Considerations

While the current design is intentionally minimal, the architecture allows for future enhancements:

- Parallel processing capabilities
- Extended command set
- Plugin system
- Performance optimizations

The design's simplicity makes it easier to maintain and extend while keeping the core functionality efficient and reliable.

# Development Workflow

The development process follows these principles:

- Maintain simplicity in both design and implementation
- Prioritize performance in architectural decisions
- Ensure robust error handling
- Keep the codebase maintainable and well-documented

This architectural approach demonstrates that sometimes less is more - by focusing on essential components and eliminating unnecessary complexity, Vex achieves its goals of simplicity, performance, and reliability in text processing tasks.