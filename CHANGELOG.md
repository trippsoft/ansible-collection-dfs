# Changelog

All notable changes to this project will be documented in this file.

## [1.1.9] - 2025-01-08

- Added Changelog.
- Updated collection README documentation.

## [1.1.8] - 2024-10-22

- *trippsc2.dfs.replication* role - Removed `os_family` subset for fact gathering step as it is not used on Windows machines.

## [1.1.7] - 2024-09-06

- *trippsc2.dfs.replication* role - Added the `no_log` tag to the `dfsr_admin_password` variable.

## [1.1.6] - 2024-08-09

- Minimum Ansible version changed from `2.14` to `2.15` due to EOL status.

## [1.1.5] - 2024-07-10

- *trippsc2.dfs.replication* role - Restructured role to allow for multiple DFS replication groups to be added at once.

## [1.1.4] - 2024-07-08

- Updated manifest file to ensure that molecule tests are not included in releases.

## [1.1.3] - 2024-07-07

- *trippsc2.dfs.replication* role - Added validation that the system is a running Windows Server as a domain member.

## [1.1.2] - 2024-06-30

- *trippsc2.dfs.replication* role - Fixed documentation to properly include role dependencies.

## [1.1.1] - 2024-06-24

- *trippsc2.dfs.replication* role - Removed steps to install `NuGet` package provider, `PowerShellGet` module, `PackageManagement` module, and `PSGallery` repository from tasks.
- *trippsc2.dfs.replication* role - Added role dependency on *trippsc2.windows.install_psgallery* role to install `NuGet` package provider, `PowerShellGet` module, `PackageManagement` module, and `PSGallery` repository.

## [1.1.0] - 2024-06-24

- Removed dependency reference to **trippsc2.general** collection.
- Added dependency reference to **trippsc2.windows** collection.
- *trippsc2.dfs.replication* role - Changed reference to *trippsc2.general.win_package_provider* module to *trippsc2.windows.win_package_provider* module.

## [1.0.1] - 2024-06-20

- *trippsc2.dfs.replication* role - Updated documentation and role metadata for readability.

## [1.0.0] - 2024-06-11

- Initial release.
- *trippsc2.dfs.replication* role - Role added.
