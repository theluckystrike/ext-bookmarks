# ext-bookmarks

A TypeScript library providing a wrapper around Chrome's bookmarks API for extension development.

## Overview

ext-bookmarks is a TypeScript library designed to simplify Chrome extension development by providing a type-safe wrapper around the browser bookmarks API. It offers a clean, promise-based interface for managing bookmarks within Chrome extensions.

## Installation

```bash
npm install @theluckystrike/ext-bookmarks
```

## Usage

```typescript
import { createApi, ApiOptions } from '@theluckystrike/ext-bookmarks';

const options: ApiOptions = {};
const api = createApi(options);
```

## API Reference

### Types

**ApiOptions**
Configuration options for the API wrapper.

**createApi(options?: ApiOptions)**
Creates and returns an API instance configured with the provided options.

## Development

Clone the repository and install dependencies:

```bash
git clone https://github.com/theluckystrike/ext-bookmarks.git
cd ext-bookmarks
npm install
```

Build the project:

```bash
npm run build
```

## License

MIT License

## About

ext-bookmarks is maintained by theluckystrike. This library is part of a collection of developer tools and Chrome extension utilities.

For more information, visit [zovo.one](https://zovo.one).
