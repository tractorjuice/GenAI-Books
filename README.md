# Wardley Map Library 🗺️

[![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-000000?style=flat&logo=vercel)](https://library.wardleymaps.ai/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Books](https://img.shields.io/badge/Books-174-blue.svg)](https://library.wardleymaps.ai/)

A comprehensive digital library of Wardley Mapping resources, strategic analysis reports, and business strategy books. Built with Vercel serverless functions and modern web technologies for optimal performance and user experience.

**🌐 Live Application:** [https://library.wardleymaps.ai/](https://library.wardleymaps.ai/)

## ✨ Features

- **📚 174+ Books**: Comprehensive collection of strategic analysis and Wardley Mapping resources
- **🔍 Smart Search**: Real-time search with category filtering and fuzzy matching
- **📖 Interactive Reading**: Table of contents navigation, responsive design, mobile-optimized
- **🎯 Auto-Categorization**: AI-powered book categorization across multiple domains
- **🔗 Smart Linking**: Deep linking to book sections, Wardley map reports, share functionality
- **⚡ High Performance**: Serverless architecture with optimized loading and caching

## 🚀 Quick Start

### For Users
Visit [library.wardleymaps.ai](https://library.wardleymaps.ai/) to browse and read books instantly.

### For Developers
```bash
# Clone the repository
git clone https://github.com/tractorjuice/GenAI-Books.git
cd GenAI-Books

# Install dependencies
npm install

# Generate book manifest
npm run generate-manifest

# Start local development
npm run test-server
```

## 📂 Project Structure

```
├── api/                    # Vercel serverless functions
│   ├── books.js           # Books listing API
│   ├── books/[id].js      # Individual book details
│   └── wardley/           # Wardley map integration
├── books/                 # Book content library (174+ books)
├── docs/                  # Comprehensive documentation
├── public/                # Frontend application
├── scripts/               # Utility scripts
└── tests/                 # Test suite
```

## 📚 Book Categories

The library covers diverse strategic domains:

- **Strategic Mapping** (53 books): Wardley Mapping methodology and applications
- **Artificial Intelligence** (89 books): GenAI, LLMs, and AI strategy
- **Business Strategy** (30 books): Strategic planning and competitive advantage  
- **Government** (10 books): Public sector transformation and policy
- **Sustainability** (15 books): Environmental and social governance
- **Healthcare** (4 books): Medical technology and health systems
- **Gaming** (4 books): AI in gaming and interactive entertainment
- **Security** (4 books): Cybersecurity and privacy frameworks

## 🛠️ Development

### Key Scripts
```bash
npm run generate-manifest      # Scan books, update manifest, and generate sitemaps
npm run generate-toc          # Generate table of contents for all books
npm run build-all            # Complete build process
```

### Sitemap Generation
The manifest generator automatically creates and updates two sitemaps:
- **Library Sitemap** (`sitemap.xml`): 200+ URLs for books, categories, and API endpoints
- **Podcast Sitemap** (`sitemap-podcast.xml`): 154+ URLs for podcast episodes from RSS feed

```bash
# Generate both sitemaps automatically
node scripts/generate-manifest.js

# Or generate podcast sitemap independently
node scripts/generate-podcast-sitemap.js
```

### Adding New Books
1. Add book directory to `books/` with `full_book.md`
2. Run `npm run generate-manifest` to update catalog and both sitemaps
3. Test with `npm run test-server`

### SEO and Search Engines
- **Library Sitemap**: Automatically generated at `/public/sitemap.xml` (accessible via `library.wardleymaps.ai/sitemap.xml`)
- **Podcast Sitemap**: Automatically generated at `/public/sitemap-podcast.xml` from RSS feed conversion
- **Auto-Updates**: Both sitemaps regenerate whenever content changes (books added/removed or new podcast episodes)
- **Coverage**: 
  - Library: 200+ URLs including all books, categories, and API endpoints
  - Podcast: 154+ URLs including episodes, pagination pages, and RSS feed
- **Search Console**: Submit both sitemaps to Google Search Console and Bing Webmaster Tools

### RSS to Sitemap Conversion
The podcast sitemap is automatically generated from the live RSS feed:
- **Source**: `https://podcast.wardleymaps.ai/feed.xml`
- **Episodes Discovered**: 135+ podcast episodes with publication dates
- **Additional Pages**: Homepage, RSS feed, and 17 pagination pages
- **Update Frequency**: Syncs with RSS feed changes automatically

### Architecture
- **Frontend**: Vanilla JavaScript with modern ES6+ features
- **Backend**: Vercel serverless functions with manifest-based discovery
- **Storage**: Git-based content management with GitHub integration
- **SEO**: Automated XML sitemap generation for both library and podcast content
- **RSS Integration**: Live RSS-to-sitemap conversion with episode discovery
- **Deployment**: Automated Vercel deployment from Development branch

### Technical Dependencies
- **Core**: Node.js, vanilla JavaScript, Vercel serverless functions
- **XML Processing**: `xml2js` for RSS feed parsing and sitemap generation
- **Testing**: Custom test suite for API endpoints and content validation
- **Build Tools**: Automated manifest generation and content discovery

## 📖 Documentation

Comprehensive documentation is available in the [`docs/`](./docs/) directory:

- **[Development Guide](./docs/README.md)** - Complete documentation index
- **[Developer Notes](./CLAUDE.md)** - Architecture and development workflows  
- **[Enhancement Roadmap](./docs/ENHANCEMENTS.md)** - Planned features and implementation
- **[Manifest System](./docs/MANIFEST.md)** - Book discovery and categorization
- **[Table of Contents](./docs/TABLE_OF_CONTENTS.md)** - TOC generation system

## 🧪 Testing

```bash
# Run all tests
npm run test-all

# Test individual components
node tests/test-books.js        # Book data verification
node tests/test-api-endpoints.js # API functionality
node tests/test-server.js       # Local development server
```

## 🤝 Contributing

We welcome contributions! Please see our development guidelines:

1. **Branch Strategy**: All development happens on the `Development` branch
2. **Code Quality**: Follow existing patterns and conventions
3. **Documentation**: Update relevant docs for any changes
4. **Testing**: Ensure all tests pass before submitting

```bash
git checkout Development
# Make your changes
npm run generate-manifest  # Update manifest and both sitemaps if adding books
npm run test-all           # Verify everything works
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Links

- **Live Application**: [library.wardleymaps.ai](https://library.wardleymaps.ai/)
- **Repository**: [GitHub](https://github.com/tractorjuice/GenAI-Books)
- **Issues**: [Bug Reports & Features](https://github.com/tractorjuice/GenAI-Books/issues)

## 🏆 Acknowledgments

This library serves the strategic thinking community by providing free access to high-quality Wardley Mapping and strategic analysis resources. Built with modern web technologies for optimal performance and user experience.

---

*Empowering strategic thinking through accessible knowledge and interactive learning.*