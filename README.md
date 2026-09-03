# @sudobility/shaperouter_lib

Business logic library for ShapeRouter with Zustand stores and endpoint templates.

## Installation

```bash
bun add @sudobility/shaperouter_lib
```

## Usage

```typescript
import { useKeysStore, useProjectsStore } from '@sudobility/shaperouter_lib';
import { ALL_TEMPLATES, applyTemplate } from '@sudobility/shaperouter_lib';

// Store access
const keys = useKeysStore(state => state.getKeys(userId));

// Apply endpoint template
const { project, endpoints } = applyTemplate(textClassifierTemplate, 'my-classifier', 'key-123');
```

## Stores

| Store | Purpose |
|-------|---------|
| `useKeysStore` | LLM API keys cache |
| `useProjectsStore` | Projects cache |
| `useEndpointsStore` | Endpoints cache |
| `useSettingsStore` | User settings cache |
| `useAnalyticsStore` | Analytics cache |

## Endpoint Templates

Pre-built templates: Text Classifier, Sentiment Analyzer, Data Extractor, Content Generator, Localization.

## Development

```bash
bun run build        # Build to dist/
bun run test         # Run Vitest (watch mode)
bun run test:run     # Run tests once
bun run typecheck    # TypeScript check
bun run lint         # ESLint
bun run verify       # Typecheck + lint + test + build
```

## Related Packages

- `@sudobility/shaperouter_client` -- API hooks (peer dependency)
- `@sudobility/shaperouter_types` -- Type definitions
- `shaperouter_app` -- Frontend consumer

## License

BUSL-1.1
