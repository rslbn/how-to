# Imporatant Setting

## Path
```yaml
path:
	data: /var/data/elasticsearch
	log: /var/log/elasticsearch
```
> modify the permissions for both data & log (rwx)

## Cluster name setting
`cluster.name: loggin-prod`

## Node name setting
`node.name: prod-data-2`

## Network host setting
> By default, Elasticsearch only binds to loopback addresses such as 127.0.0.1 and [::1]. This is sufficient to run a cluster of one or more nodes on a single server for dev and testing, but a resilient production cluster must involve nodes on other servers. There are meny network settigns but usually all you need to configure is
`network.host: 192.168.1.10`

## Jvm configuration
> file path: /elasticsearch/config/jvm.options

### Set the JVM heap size
> By default, Elasticsaerch automatically sets the JVM heap size based on a node's roles and total  memory. Using the default sizing is recommended for most production env.
> To override the default heap size, set the minimum and max heap size settings. The max and min values must be the same.
> The heap size should be based on the available RAM:
- Set **Xmx** and **Xms** to no more than 50% of your total memory. Elasticsearch requires memory for purposes other than the JVM heap. For example, on the OS's filesystem cache for efficient access to files. The JVM itself also requires some memory. It's normal for Elasticsearch to use more memory than limit configured with **Xmx** setting.
`-Xms512g`
`-Xmx512g`

