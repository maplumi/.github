# Maplumi Labs

**Geospatial Intelligence & Data Infrastructure for Humanitarian Insights**

Maplumi Labs is a research and development organization focused on building open-source geospatial tools, data infrastructure, and innovative technologies that bridge the gap between complex geographic data and actionable insights. We specialize in creating accessible, high-performance solutions for data visualization, humanitarian response, and advanced computational research.

---

## 🌍 Our Mission

We believe that geographic data should be:
- **Accessible** – Available to organizations and researchers without complex barriers
- **Performant** – Fast enough to handle real-world datasets at scale
- **Interoperable** – Compatible with industry-standard tools and workflows
- **Open** – Built on open-source principles with transparent methodologies

Our work spans three core areas:
1. **Geospatial Data Visualization** – Making complex geographic data understandable and actionable
2. **Humanitarian Data Infrastructure** – Providing critical boundary and classification data for crisis response
3. **Advanced Computational Research** – Exploring novel approaches to data processing and cognitive systems

---

## 🛠️ Our Tools & Projects

### **Maplumi Power BI Visual**
*Production-ready geospatial visualization for Microsoft Power BI*

Transform your geographic data into compelling visual stories with our flagship Power BI custom visual. Designed for analysts, researchers, and decision-makers who need professional-quality maps without GIS expertise.

**Key Features:**
- **Dual-layer rendering** – Choropleth regions and scaled circles work together or separately
- **Multiple rendering engines** – SVG (high quality), Canvas (fast), and WebGL (GPU-accelerated) with automatic fallback
- **Smart boundary integration** – Built-in GeoBoundaries support plus custom TopoJSON/GeoJSON
- **Professional cartography** – Equal interval, quantile, and natural breaks classification with customizable color ramps
- **Enterprise-ready** – Handles 30,000+ rows with topology-preserving simplification
- **Modern basemaps** – OpenStreetMap, Mapbox, and MapTiler integration
- **Interactive features** – Legends, tooltips, cross-filtering, zoom controls

**Technical Highlights:**
- Built on OpenLayers, D3, and Power BI Visuals API
- Comprehensive test coverage with Jest
- Automated CI/CD with semantic versioning
- HTTPS-only with security guardrails (CORS, open-redirect protection, validated P-codes)

**Repository:** [maplumi/maplumi-pbi](https://github.com/maplumi/maplumi-pbi)  
**Documentation:** [maplumi/maplumi-pbi-docs](https://github.com/maplumi/maplumi-pbi-docs)

---

### **GeoBoundaries Lite**
*Lightweight, CDN-ready administrative boundary data delivery*

A curated distribution system for global administrative boundaries that makes it trivial to integrate country, state/province, and district-level boundaries into applications.

**What We Provide:**
- **Three release tiers:**
  - `gbopen` – General-purpose open boundaries
  - `gbhumanitarian` – Humanitarian response boundaries
  - `gbauthoritative` – Authoritative government boundaries
- **Three administrative levels:**
  - `admin0` – Country boundaries
  - `admin1` – States/provinces/regions
  - `admin2` – Districts/counties (where available)

**Key Features:**
- **CDN delivery via jsDelivr** – Tag-pinned, versioned access to TopoJSON files
- **Compact manifest** – Single `index.json` for programmatic discovery
- **Size-optimized** – Automated pruning of files >50MB, topology-preserving simplification
- **HDX enrichment** – Optional integration with Humanitarian Data Exchange metadata
- **Mapbox tileset support** – Upload CGAZ (Comprehensive Global Administrative Zones) as vector tilesets

**Use Cases:**
- Web mapping applications needing administrative boundaries
- Humanitarian response platforms requiring standardized P-codes
- Data visualization tools that need lightweight geometry
- Mobile applications with bandwidth constraints

**Repository:** [maplumi/geoboundaries-lite](https://github.com/maplumi/geoboundaries-lite)

---

### **IPC Areas Data Toolkit**
*Integrated Food Security Phase Classification boundary automation*

An automated pipeline for fetching, harmonizing, and distributing IPC (Integrated Food Security Phase Classification) area boundaries from the IPC Global Platform API.

**What It Does:**
- **Automated data collection** – Scheduled weekly fetches from IPC API with rate limiting and retry logic
- **Multi-year aggregation** – Per-year TopoJSON files plus combined country datasets
- **Global dataset** – Single `global_areas.topojson` merging all countries and years
- **Deduplication** – Smart merging by IPC ID with coordinate precision control
- **CDN delivery** – Tag-based distribution via jsDelivr with programmatic index

**Key Features:**
- **Per-year snapshots** – Preserve individual assessment data for historical analysis
- **Combined country files** – Deduplicated multi-year boundaries per country
- **Global aggregation** – Single file spanning all available IPC assessments
- **Coordinate precision** – Configurable rounding (default: 4 decimal places)
- **Topology simplification** – Shapely-based simplification with adjustable tolerance

**Use Cases:**
- Food security monitoring dashboards
- Humanitarian needs assessments
- Early warning systems for famine/crisis
- Research on food security trends over time

**Technical Stack:**
- Python 3.8+ with topojson, shapely, requests
- GitHub Actions automation for scheduled updates
- IPC Global Platform API integration

**Repository:** [maplumi/ipc-areas](https://github.com/maplumi/ipc-areas)

---

### **Braine Web**
*Experimental cognitive substrate web demonstration*

An exploratory project investigating novel approaches to cognitive computing and data substrate architectures. Built with WebAssembly (Rust compiled to WASM), this experimental demo showcases research into alternative computational paradigms.

**Focus Areas:**
- **Cognitive substrate architectures** – Exploring how data can be organized and processed in brain-inspired patterns
- **WebAssembly performance** – Leveraging WASM for high-performance web computations
- **Experimental interfaces** – Novel interaction patterns for complex data systems

**Status:** Experimental research prototype

**Repository:** [maplumi/braine-web](https://github.com/maplumi/braine-web)

---

## 📊 Research Areas

### **Geospatial Data Processing**
We develop efficient algorithms and workflows for processing large-scale geographic datasets:
- Topology-preserving simplification for web delivery
- Multi-format conversion (GeoJSON, TopoJSON, Shapefile)
- Coordinate precision optimization
- Automated data pipeline orchestration

### **Humanitarian Data Standards**
We contribute to and implement humanitarian data standards:
- **P-code integration** – Administrative boundary codes (HXL, COD-AB)
- **IPC classification** – Food security phase classification
- **HDX metadata** – Humanitarian Data Exchange enrichment
- **CGAZ boundaries** – Comprehensive Global Administrative Zones

### **Performance Optimization**
We prioritize performance across our tools:
- **Multi-engine rendering** – SVG, Canvas, WebGL with intelligent fallback
- **Lazy loading** – Fetch data only when needed
- **CDN distribution** – Leverage edge networks for global delivery
- **Client-side caching** – Reduce redundant network requests
- **Data reduction** – Smart decimation while preserving visual fidelity

### **Advanced Computation**
We explore emerging computational paradigms:
- **WebAssembly research** – High-performance web computation
- **Cognitive architectures** – Alternative data processing models
- **GPU acceleration** – WebGL for geospatial rendering

---

## 🔧 Technology Stack

### **Core Technologies**
- **Languages:** TypeScript, JavaScript, Python, Rust
- **Geospatial:** OpenLayers, D3.js, topojson, shapely, geojson
- **Visualization:** Power BI Visuals API, WebGL, Canvas API, SVG
- **Data Processing:** simple-statistics, chroma.js, NumPy
- **Build & Test:** Jest, webpack, npm, pip

### **Infrastructure**
- **Version Control:** Git, GitHub
- **CI/CD:** GitHub Actions
- **Distribution:** jsDelivr CDN, npm, Power BI AppSource
- **APIs:** IPC Global Platform, HDX, GeoBoundaries, Mapbox, MapTiler

### **Data Formats**
- **Geographic:** TopoJSON, GeoJSON, Shapefile, WKT
- **Classification:** Equal Interval, Quantile, Natural Breaks (Jenks)
- **Coordinates:** WGS84 (EPSG:4326), Web Mercator (EPSG:3857)

---

## 🌟 Key Differentiators

### **1. User-Centric Design**
We build tools that analysts and researchers can actually use:
- Clear documentation with step-by-step tutorials
- Sensible defaults that work out of the box
- Progressive disclosure – simple tasks are simple, complex tasks are possible

### **2. Production-Quality Engineering**
Our tools are built for real-world use:
- Comprehensive automated testing
- Security-first architecture (HTTPS-only, CORS, input validation)
- Performance monitoring and optimization
- Semantic versioning and release management

### **3. Open Source Commitment**
Everything we build is open:
- MIT licensed (where applicable)
- Public repositories with issue tracking
- Transparent development process
- Community contributions welcome

### **4. Data Accessibility**
We make complex data simple:
- CDN-ready distribution (jsDelivr, GitHub Pages)
- Tag-based versioning for reproducibility
- Compact manifests for programmatic discovery
- Multiple format options (TopoJSON, GeoJSON)

### **5. Interoperability**
Our tools work with industry standards:
- Power BI integration (maplumi-pbi)
- Mapbox and MapTiler support
- Standard geospatial formats (GeoJSON, TopoJSON)
- REST APIs and static file delivery

---

## 🎯 Use Cases

### **Humanitarian Response**
- **Food security monitoring** with IPC Areas data
- **Administrative boundary mapping** with GeoBoundaries
- **Crisis visualization** in Power BI dashboards
- **Needs assessment mapping** with choropleth classification

### **Business Intelligence**
- **Sales territory analysis** with custom boundaries
- **Market penetration maps** with scaled circles
- **Regional performance dashboards** in Power BI
- **Geographic KPI tracking** with cross-filtering

### **Research & Academia**
- **Spatial analysis** with standardized boundaries
- **Demographic visualization** with classification algorithms
- **Multi-temporal analysis** with historical IPC data
- **Publication-quality cartography** with custom color ramps

### **Government & Policy**
- **Public health surveillance** with district-level boundaries
- **Electoral mapping** with authoritative boundaries
- **Resource allocation** with population-weighted metrics
- **Service delivery planning** with administrative hierarchies

---

## 📈 Impact

Our tools are designed to support:
- **Humanitarian organizations** responding to food security crises
- **Government agencies** managing public services and resources
- **Research institutions** conducting spatial analysis
- **Business analysts** making data-driven geographic decisions
- **NGOs** tracking program implementation and impact

---

## 🤝 Contributing

We welcome contributions across all our projects:
- **Bug reports** – Help us improve stability
- **Feature requests** – Share your use cases and needs
- **Code contributions** – Submit PRs with tests
- **Documentation** – Improve guides and examples
- **Data quality** – Report boundary or classification issues

See individual repository CONTRIBUTING.md files for specific guidelines.

---

## 📫 Connect With Us

- **GitHub Organization:** [github.com/maplumi](https://github.com/maplumi)
- **Report Issues:** Use repository-specific issue trackers
- **Discussions:** GitHub Discussions on individual repos

---

## 📄 Licensing

Our projects use open-source licenses:
- **Code:** MIT License (most projects)
- **Data:** Follows source terms (GeoBoundaries, IPC Platform)
- **Documentation:** Creative Commons (where applicable)

Always review individual repository LICENSE files for specific terms.

---

## 🔮 Future Directions

We're actively exploring:
- **Real-time data pipelines** for crisis response
- **Enhanced WebGL rendering** for larger datasets
- **Machine learning integration** for automated classification
- **Mobile-first interfaces** for field data collection
- **Cognitive computing substrates** for novel data processing paradigms

---

*Building better tools for a data-driven world, one boundary at a time.*