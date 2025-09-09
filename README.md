# TechHalo Chat React Setup

This provides steps to integrate the TechHalo Chat Widget into React applications.

## Installation

Install the package using npm:

```bash
npm install @techhalo/chat
```

## Quick Start

### Step 1: Create a React Component

Create a new React component file (e.g., `HaloWidget.tsx`) and add the following code:

```typescript
import React from 'react';
import '@techhalo/chat';
import type { HaloChatProps } from '@techhalo/chat';

export default function HaloWidget(): React.JSX.Element {
  const props: HaloChatProps = {
    projectId: "Your unique project identifier",
    position: "bottom-right"
  };

  return React.createElement('halo-chat', props as HaloChatProps);
}
```

### Step 2: Use the Component

Import and use the `HaloWidget` component anywhere in your React application:

```typescript
import React from 'react';
import HaloWidget from './path/to/HaloWidget';

function App() {
  return (
    <div className="App">
      {/* Your other components */}
      {/* Add the Halo chat widget */}
      <HaloWidget />
    </div>
  );
}

export default App;
```

## Configuration

The `HaloChatProps` interface accepts the following properties:

| Property | Type | Required | Description |
|----------|------|----------|-------------|
| `projectId` | `string` | Yes | Your unique project identifier |
| `position` | `string` | No | Position of the chat widget (e.g., "bottom-right", "bottom-left") |

