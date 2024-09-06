<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: trippsc2.dfs.replication
Version: 1.1.7

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
| dfsr_admin_user | <p>The user account to be used when configuring DFS Replication.</p> | str | yes |  |  |
| dfsr_admin_password | <p>The password for the *dfs_admin_user* user account.</p> | str | yes |  |  |
| dfsr_default_primary_member | <p>Whether the server should default to being the primary member for folders in DFS Replication groups.</p> | bool | no |  | false |
| dfsr_default_read_only | <p>Whether the server should default to being a read-only member for folders in DFS Replication groups.</p> | bool | no |  | false |
| dfsr_groups | <p>A list of DFS Replication groups to configure.</p> | list of dicts of 'dfsr_groups' options | yes |  |  |

### Options for dfsr_groups
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| name | <p>The name of the DFS Replication group to configure.</p> | str | yes |  |  |
| primary_member | <p>Whether the server should default to being the primary member for folders in this DFS Replication group.</p> | bool | no |  | false |
| read_only | <p>Whether the server should default to being a read-only member for folders in this DFS Replication group.</p> | bool | no |  | false |
| folders | <p>A list of folders to configure in this DFS Replication group.</p> | list of dicts of 'folders' options | yes |  |  |
| members | <p>A list of the fully qualified domain names (FQDN) of the member servers of this DFS Replication group.</p> | list of 'str' | yes |  |  |

### Options for dfsr_groups > folders
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| name | <p>The name of the folder to configure.</p> | str | yes |  |  |
| path | <p>The local path of the folder.</p> | path | yes |  |  |
| primary_member | <p>Whether the member server is the primary member for the folder.</p><p>This defaults to the *primary_member* value for the group or the *dfsr_default_primary_member* value in that order.</p> | bool | no |  | false |
| read_only | <p>Whether the member server is read-only for the folder.</p><p>This defaults to the *read_only* value for the group or the *dfsr_default_read_only* value in that order.</p> | bool | no |  | false |
| staging_quota | <p>The staging quota for the folder in MB.</p><p>This should be equal to the sum of the sizes of the largest 32 files to be replicated.</p> | int | no |  | 4096 |


## License
MIT

## Author and Project Information
Jim Tarpley
<!-- END_ANSIBLE_DOCS -->
