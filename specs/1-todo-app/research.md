# Research & Design Decisions: Phase-I In-Memory Python Console-Based Todo Application

## Decision: Task ID Generation Method
**Rationale**: Using Python's built-in `uuid.uuid4()` for unique ID generation to ensure uniqueness without maintaining counters. This is efficient and suitable for the in-memory scope.
**Alternatives considered**: Sequential integer IDs, timestamp-based IDs. UUIDs were chosen for their guaranteed uniqueness without coordination.

## Decision: In-Memory Storage Implementation
**Rationale**: Using Python dictionary to store tasks with UUID as key for O(1) lookup performance, which meets the performance requirements (SC-002).
**Alternatives considered**: Lists, sets, other data structures. Dictionary provides the best balance of performance and functionality.

## Decision: CLI Framework Selection
**Rationale**: Using Python's built-in `input()` and `print()` functions for maximum simplicity and compatibility with Python 3.13+, without adding external dependencies.
**Alternatives considered**: argparse, click, typer. The simple built-in approach is sufficient for the console-based requirements.

## Decision: Task Class Design
**Rationale**: Implementing Task as a dataclass for clean, readable code with automatic `__init__`, `__repr__`, and other methods while maintaining immutability where possible.
**Alternatives considered**: Regular classes, named tuples. Dataclass provides the right balance of functionality and simplicity.

## Decision: Error Handling Approach
**Rationale**: Using Python exceptions with custom exception classes for different error types, allowing for specific error messages and handling while maintaining application stability.
**Alternatives considered**: Return codes, boolean flags. Exceptions provide cleaner separation of success and error paths.