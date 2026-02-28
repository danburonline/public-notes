#core/softwaredevelopment

![pull-approach](../../_inbox/attachments/pull-approach.png)

Pull-based deployments involve **target environments autonomously pulling updates from a repository instead of receiving them through external pushes.**

## Characteristics

- **Autonomy**: Environments independently pull updates.
- **Decentralisation**: Shifts responsibility to individual environments.
- **Scalability**: Efficient scaling as each node manages its own updates.
- **Security**: Reduced risk of unauthorised pushes.

## Advantages

- **Flexibility**: Each environment updates on its own schedule.
- **Version Control**: Easy tracking of changes through source repositories.

## Use Cases

- Kubernetes clusters pulling container images.
- Configuration management with tools like Ansible or Puppet.
