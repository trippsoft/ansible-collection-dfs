<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: trippsc2.dfs.replication
Version: 1.1.2

This role configures DFS Replication on a Windows Server machine.

## Requirements

| Platform | Versions |
| -------- | -------- |
| Windows | <ul><li>2019</li><li>2022</li></ul> |

## Dependencies
| Role |
| ---- |
| trippsc2.windows.install_psgallery |

| Collection |
| ---------- |
| ansible.windows |
| community.windows |
| trippsc2.windows |

## Role Arguments
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| dfsr_admin_user | <p>The user account to use for configuring DFS Replication.</p> | str | yes |  |  |
| dfsr_admin_password | <p>The password for the user account to use for configuring DFS Replication.</p> | str | yes |  |  |
| dfsr_members | <p>A list of member servers to configure for DFS Replication.</p> | list of 'str' | yes |  |  |
| dfsr_primary_member | <p>Whether the member server is the primary member by default.</p><p>This can be overridden per folder.</p> | bool | no |  | false |
| dfsr_read_only | <p>Whether the member server is read-only by default.</p><p>This can be overridden per folder.</p> | bool | no |  | false |
| dfsr_folders | <p>A list of folders to configure for DFS Replication.</p> | list of dicts of 'dfsr_folders' options | no |  |  |

### Options for dfsr_folders
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| name | <p>The name of the folder to configure for DFS Replication.</p> | str | yes |  |  |
| path | <p>The local path of the folder to configure for DFS Replication.</p> | path | yes |  |  |
| primary_member | <p>Whether the member server is the primary member for the folder.</p><p>If provided, this overrides the `dfsr_primary_member` value.</p> | bool | no |  | false |
| read_only | <p>Whether the member server is read-only for the folder.</p><p>If provided, this overrides the `dfsr_read_only` value.</p> | bool | no |  | false |
| staging_quota | <p>The staging quota for the folder.</p> | int | no |  | 4096 |


## License
MIT

## Author and Project Information
Jim Tarpley
<!-- END_ANSIBLE_DOCS -->
