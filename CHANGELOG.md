# Changelog

All notable changes to this project will be documented in this file.

## [1.1.12] - 2025-06-10

### Collection

- Corrected missing or extra dependencies.

## [1.1.11] - 2025-06-10

### Collection

- Changed repository URL to use GitHub Organization.

## [1.1.10] - 2025-03-10

### Role - replication

- Fixed include/import tasks paths.

## [1.1.9] - 2025-01-08

### Collection

- Added Changelog.
- Updated collection README documentation.

## [1.1.8] - 2024-10-22

### Role - replication

- Removed `os_family` subset for fact gathering step as it is not used on Windows machines.

## [1.1.7] - 2024-09-06

### Role - replication

- Added the `no_log` tag to the `dfsr_admin_password` variable.

## [1.1.6] - 2024-08-09

### Collection

- Minimum Ansible version changed from `2.14` to `2.15` due to EOL status.

## [1.1.5] - 2024-07-10

### Role - replication

- Restructured role to allow for multiple DFS replication groups to be added at once.

## [1.1.4] - 2024-07-08

### Collection

- Updated manifest file to ensure that molecule tests are not included in releases.

## [1.1.3] - 2024-07-07

### Role - replication

- Added validation that the system is a running Windows Server as a domain member.

## [1.1.2] - 2024-06-30

### Role - replication

- Fixed documentation to properly include role dependencies.

## [1.1.1] - 2024-06-24

### Role - replication

- Removed steps to install `NuGet` package provider, `PowerShellGet` module, `PackageManagement` module, and `PSGallery` repository from tasks.
- Added role dependency on *trippsc2.windows.install_psgallery* role to install `NuGet` package provider, `PowerShellGet` module, `PackageManagement` module, and `PSGallery` repository.

## [1.1.0] - 2024-06-24

### Collection

- Removed dependency reference to **trippsc2.general** collection.
- Added dependency reference to **trippsc2.windows** collection.

### Role - replication

- Changed reference to *trippsc2.general.win_package_provider* module to *trippsc2.windows.win_package_provider* module.

## [1.0.1] - 2024-06-20

### Role - replication

- Updated documentation and role metadata for readability.

## [1.0.0] - 2024-06-11

### Collection

- Initial release.
- *replication* role added.
