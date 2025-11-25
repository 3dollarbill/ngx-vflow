# Custom Changes

This document tracks modifications made to the ngx-vflow library.

## Changes Made

### SharedDynamicNode Interface

- **`controlledByResizer` field**
  - Type: `WritableSignal<boolean>` (optional, default: `true`)
  - Location: `projects/ngx-vflow-lib/src/lib/vflow/interfaces/node.interface.ts`
  - Dynamic nodes can now specify if they are controlled by a resizer, initialized from node data if present (otherwise defaults to `true`).

### NodeModel

- **Initialization of `controlledByResizer`**
  - The `NodeModel` constructor now checks for `controlledByResizer` in the node data.
  - If present, these values are used; otherwise, `controlledByResizer` defaults to `true`.
  - Location: `projects/ngx-vflow-lib/src/lib/vflow/models/node.model.ts`

## Files Modified

- `projects/ngx-vflow-lib/src/lib/vflow/interfaces/node.interface.ts`
- `projects/ngx-vflow-lib/src/lib/vflow/models/node.model.ts`
