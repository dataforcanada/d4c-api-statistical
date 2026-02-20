# d4c-api

A multi-language client for accessing Canadian data. This repository provides a unified interface to fetch:
- Statistical data processed by the [d4c-datapkg-statistical](https://github.com/dataforcanada/d4c-datapkg-statistical) repository.

## Purpose

The goal of this project is to provide a consistent way to query metadata and raw data across different programming environments. As the connectivity and retrieval layer for the **Data for Canada (d4c)** project, this API facilitates access to a decentralized, cloud-native open data infrastructure for Canada.

## Core Technologies

This service layer is built to interface with modern cloud-native formats while maintaining broad compatibility:

* **[FAIR Data Catalogue](https://stac-geoparquet.org/):** For cataloging and discovering underlying datasets.
* **[GeoParquet](https://geoparquet.org/):** An efficient, columnar storage format for vector data, providing the high-performance backend for our services.
* **[GeoZarr](https://github.com/zarr-developers/geozarr-spec):** For multidimensional data processing and visualization.
* **HTTP & [P2P](https://tixati.com/specs/bittorrent):** For efficient, decentralized data retrieval and backend distribution.

## Multi-Language Support

The core connectivity logic is written in Rust and exported to other languages. This ensures that API calls, authentication methods, and data handling remain identical across all platforms.

- **Rust:** The core crate for direct system-level access and performance-critical tasks.
- **Python:** Idiomatic bindings.
- **R:** Native wrappers.
- **[Other](https://github.com/dataforcanada/d4c-api-statistical/issues)**.

## Repository Structure

We separate the shared core from the language-specific wrappers:

- **core/**: Rust source code handling HTTP requests, API authentication, and decentralized protocol logic.
- **bindings/**: Language-specific implementations for Python, R, and **[Other](https://github.com/dataforcanada/d4c-api-statistical/issues)**.
- **labs/**: Experimental area for testing new API endpoints or protocol implementations.

## Contributing

New features or bug fixes for API connections should be implemented in the `core/` directory. Enhancements to the user experience for a specific language should be made in the `bindings/` folder.

All contributors must be verified via **[Vouch](https://github.com/mitchellh/vouch)** before their pull requests are reviewed.
