# ext-bookmarks

[![npm version](https://img.shields.io/npm/v/@theluckystrike/ext-bookmarks)](https://npmjs.com/package/@theluckystrike/ext-bookmarks)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue.svg)](https://www.typescriptlang.org/)
[![CI Status](https://github.com/theluckystrike/ext-bookmarks/actions/workflows/ci.yml/badge.svg)](https://github.com/theluckystrike/ext-bookmarks/actions)
[![Discord](https://img.shields.io/badge/Discord-Zovo-blueviolet.svg?logo=discord)](https://discord.gg/zovo)
[![Website](https://img.shields.io/badge/Website-zovo.one-blue)](https://zovo.one)
[![GitHub Stars](https://img.shields.io/github/stars/theluckystrike/ext-bookmarks?style=social)](https://github.com/theluckystrike/ext-bookmarks)

> Chrome Extension bookmarks API wrapper with enhanced features.

Part of the [Zovo](https://zovo.one) family of privacy-first Chrome extensions and developer tools.

## Overview

`ext-bookmarks` is a comprehensive TypeScript wrapper around Chrome's bookmarks API, providing enhanced functionality, better type safety, and modern async/await patterns for extension development.

## Features

- ✅ **Promise-based API** - Modern async/await syntax
- ✅ **TypeScript Support** - Fully typed for better developer experience
- ✅ **Enhanced Methods** - Additional utility methods beyond Chrome API
- ✅ **MV3 Compatible** - Works with Manifest V3 extensions
- ✅ **Folder Management** - Easy bookmark folder operations
- ✅ **Privacy-First** - No data collection, all local

## Installation

### From npm

```bash
npm install @theluckystrike/ext-bookmarks
```

### From Source

```bash
# Clone the repository
git clone https://github.com/theluckystrike/ext-bookmarks.git
cd ext-bookmarks

# Install dependencies
npm install

# Build the project
npm run build
```

## Usage

### Basic Operations

```typescript
import { Bookmarks, createBookmark, getBookmarks, searchBookmarks } from '@theluckystrike/ext-bookmarks';

const bookmarks = new Bookmarks();

// Create a bookmark
const bookmark = await createBookmark({
  title: 'Example',
  url: 'https://example.com'
});

// Get all bookmarks
const all = await getBookmarks();

// Search bookmarks
const results = await searchBookmarks('example');
```

### Folder Operations

```typescript
import { createFolder, moveBookmark, deleteBookmark } from '@theluckystrike/ext-bookmarks';

// Create a folder
const folder = await createFolder({
  title: 'My Folder',
  parentId: '0'
});

// Move bookmark to folder
await moveBookmark(bookmarkId, folder.id);

// Delete bookmark
await deleteBookmark(bookmarkId);
```

## API Reference

### Functions

| Function | Description |
|----------|-------------|
| `createBookmark(props)` | Create a new bookmark |
| `createFolder(props)` | Create a bookmark folder |
| `getBookmarks(rootId?)` | Get bookmark tree |
| `searchBookmarks(query)` | Search bookmarks |
| `updateBookmark(id, props)` | Update bookmark |
| `moveBookmark(id, destination)` | Move bookmark |
| `deleteBookmark(id)` | Delete bookmark |

## Related Packages

This package is part of the Zovo extension bookmarks ecosystem:

- [ext-bookmarks-api](https://github.com/theluckystrike/ext-bookmarks-api) - Bookmarks API
- [ext-bookmarks-manager](https://github.com/theluckystrike/ext-bookmarks-manager) - Bookmark manager
- [ext-bookmark-sync](https://github.com/theluckystrike/ext-bookmark-sync) - Bookmark sync
- [ext-bookmark-edu](https://github.com/theluckystrike/ext-bookmark-edu) - Educational bookmarks

## Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/bookmarks-improvement`
3. **Make** your changes
4. **Test** your changes: `npm test`
5. **Commit** your changes: `git commit -m 'Add new feature'`
6. **Push** to the branch: `git push origin feature/bookmarks-improvement`
7. **Submit** a Pull Request

### Development Setup

```bash
# Clone the repository
git clone https://github.com/theluckystrike/ext-bookmarks.git
cd ext-bookmarks

# Install dependencies
npm install

# Run tests
npm test

# Build
npm run build
```

## Built by Zovo

Part of the [Zovo](https://zovo.one) developer tools family — privacy-first Chrome extensions built by developers, for developers.

## See Also

### Related Zovo Repositories

- [zovo-extension-template](https://github.com/theluckystrike/zovo-extension-template) - Boilerplate for building privacy-first Chrome extensions
- [zovo-types-webext](https://github.com/theluckystrike/zovo-types-webext) - Comprehensive TypeScript type definitions for browser extensions
- [zovo-permissions-scanner](https://github.com/theluckystrike/zovo-permissions-scanner) - Privacy scanner for Chrome extensions
- [zovo-indexer](https://github.com/theluckystrike/zovo-indexer) - Indexing service for Zovo extensions

### Zovo Chrome Extensions

- [Zovo Tab Manager](https://chrome.google.com/webstore/detail/zovo-tab-manager) - Manage tabs efficiently
- [Zovo Focus](https://chrome.google.com/webstore/detail/zovo-focus) - Block distractions
- [Zovo Permissions Scanner](https://chrome.google.com/webstore/detail/zovo-permissions-scanner) - Check extension privacy grades

Visit [zovo.one](https://zovo.one) for more information.

## License

MIT - [Zovo](https://zovo.one)

---

*Built by developers, for developers. No compromises on privacy.*
