<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: trippsc2.dfs.replication
Version: 1.0.0

This role configures DFS Replication on a Windows Server machine.

## Requirements

| Platform | Versions |
| -------- | -------- |
| Windows | <ul><li>2019</li><li>2022</li></ul> |

## Dependencies

| Collection |
| ---------- |
| ansible.windows |
| community.windows |
| trippsc2.general |

## Role Arguments
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| dfsr_admin_user | The user account to use for configuring DFS Replication. | str | yes |  |  |
| dfsr_admin_password | The password for the user account to use for configuring DFS Replication. | str | yes |  |  |
| dfsr_members | A list of member servers to configure for DFS Replication. | list of 'str' | yes |  |  |
| dfsr_primary_member | Whether the member server is the primary member by default. This can be overridden per folder. | bool | no |  | false |
| dfsr_read_only | Whether the member server is read-only by default. This can be overridden per folder. | bool | no |  | false |
| dfsr_folders | A list of folders to configure for DFS Replication. | list of dicts of 'dfsr_folders' options | no |  |  |

### Options for dfsr_folders
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| name | The name of the folder to configure for DFS Replication. | str | yes |  |  |
| path | The local path of the folder to configure for DFS Replication. | path | yes |  |  |
| primary_member | Whether the member server is the primary member for the folder. If provided, this overrides the `dfsr_primary_member` value. | bool | no |  | false |
| read_only | Whether the member server is read-only for the folder. If provided, this overrides the `dfsr_read_only` value. | bool | no |  | false |
| staging_quota | The staging quota for the folder. | int | no |  | 4096 |


## License
MIT

## Author and Project Information
Jim Tarpley
<!-- END_ANSIBLE_DOCS -->
