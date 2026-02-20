# d4c-api-statistical

A multi-language client for accessing Canadian statistical web data. This repository provides a unified interface to fetch statistical data processed by the [d4c-datapkg-statistical](https://github.com/dataforcanada/d4c-datapkg-statistical) repository.

## Purpose

The goal of this project is to provide a consistent way to query statistical metadata and raw tables across different programming environments. As the connectivity and retrieval layer for the **Data for Canada (d4c)** project, this API facilitates access to a decentralized, cloud-native open data infrastructure for Canada.

## Core Technologies

The client is designed to interface with modern data distribution protocols:

- **[STAC](https://stac-geoparquet.org/) & [GeoZarr](https://github.com/zarr-developers/geozarr-spec):** For metadata discovery and high-performance multidimensional data access.
- **HTTP Seeding & BitTorrent:** For decentralized data distribution and efficient retrieval.

## Multi-Language Support

The core connectivity logic is written in Rust and exported to other languages. This ensures that API calls, authentication methods, and data handling remain identical across all platforms.

- **Rust:** The core crate for direct system-level access and performance-critical tasks.
- **Python:** Idiomatic bindings optimized for data science and machine learning workflows.
- **R:** Native wrappers designed for statistical analysis and reporting.
- **[Other](https://github.com/dataforcanada/d4c-api-statistical/issues)**

## Repository Structure

We separate the shared core from the language-specific wrappers:

- **core/**: Rust source code handling HTTP requests, API authentication, and decentralized protocol logic.
- **bindings/**: Language-specific implementations for Python and R.
- **labs/**: Experimental area for testing new API endpoints or protocol implementations.

## Contributing

New features or bug fixes for API connections should be implemented in the `core/` directory. Enhancements to the user experience for a specific language should be made in the `bindings/` folder.

All contributors must be verified via **[Vouch](https://github.com/mitchellh/vouch)** before their pull requests are reviewed.
