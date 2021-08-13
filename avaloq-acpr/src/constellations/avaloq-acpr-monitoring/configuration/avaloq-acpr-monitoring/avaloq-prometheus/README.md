# AvaloqParameters

| Name                                                          | Description                                                                                                                                                                                   | Required | Default value                                                |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------|
| OPENSHIFT_VERSION                                             | OpenShift version where this constellation is deployed to. Valid values are 3 or 4.                                                                                                           | true     | 4                                                            |
| OPENSHIFT_NAMESPACE                                           | The namespace used on Openshift where this constellation is deployed to.                                                                                                                      | true     | acpr-monitoring                                              |
| AVALOQ_PROMETHEUS_DEPLOY_SECRET                               | Set to 'false' if you don't want to deploy secrets. It can be useful when using Sealed Secrets                                                                                                | true     | true                                                         |
| AVALOQ_PROMETHEUS_DEPLOY_PVC                                  | Set to 'false' if you don't want to deploy PVCs                                                                                                                                               | true     | true                                                         |
| AVALOQ_PROMETHEUS_ALERTS                                      | Enables or disable deploy of Prometheus alerts                                                                                                                                                | true     | true                                                         |
| AVALOQ_PROMETHEUS_SESSION_SECRET                              | Secret string used to encrypt sessions                                                                                                                                                        | true     |                                                              |
| AVALOQ_REDHAT_CONTAINER_IMAGE_REGISTRY                        | URL of the container image registry containing the Red Hat images. Must end with "/", unless you set it to null                                                                               | false    | registry.service.avaloq.com/                                 |
| AVALOQ_CONTAINER_IMAGE_REGISTRY                               | URL of the container image registry. Must end with "/", unless you set it to null                                                                                                             | false    | registry.service.avaloq.com/                                 |
| AVALOQ_PROMETHEUS_OPENSHIFT_MONITORING_ROUTE                  | Route to Prometheus in 'openshift-monitorng' namespace                                                                                                                                        | false    | acpr-monitoring                                              |
| AVALOQ_PROMETHEUS_OPENSHIFT_MONITORING_PASSWORD               | Password of user used to login to Prometheus in 'openshift-monitorng' namespace                                                                                                               | false    | acpr-monitoring                                              |
| AVALOQ_PROMETHEUS_OPENSHIFT_MONITORING_USERNAME               | Username of user used to login to Prometheus in 'openshift-monitorng' namespace                                                                                                               | false    |                                                              |
| AVALOQ_PROMETHEUS_CONTAINER_IMAGE_PULL_POLICY                 | The pull policy to use for the container image. Valid values are `IfNotPresent` and `Always`, default is `IfNotPresent`.                                                                      | false    | IfNotPresent                                                 |
| AVALOQ_PROMETHEUS_CLUSTER_NAME                                | This variable is used if multiple Prometheus instances are federated                                                                                                                          | false    |                                                              |
| AVALOQ_PROMETHEUS_ETCD_NODES                                  | List of all etcd nodes within the cluster                                                                                                                                                     | false    |                                                              |
| AVALOQ_PROMETHEUS_ROUTE_HOSTNAME                              | Select a hostname to use to access Prometheus. If empty, OpenShift generates the hostname automatically                                                                                       | false    |                                                              |
| AVALOQ_PROMETHEUS_SHOW_HTPASSWD_FORM                          | Show or hide htpasswd form in Promethues oAuth proxy                                                                                                                                          | false    | false                                                        |
| AVALOQ_PROMETHEUS_REPLICAS                                    | Number of replicas of Prometheus                                                                                                                                                              | false    | 1                                                            |
| AVALOQ_PROMETHEUS_CONTAINER_IMAGE                             |                                                                                                                                                                                               | false    | openshift3/prometheus:v3.11.465                              |
| AVALOQ_PROMETHEUS_PROXY_CONTAINER_IMAGE                       |                                                                                                                                                                                               | false    | openshift3/oauth-proxy:v3.11.465                             |
| AVALOQ_PROMETHEUS_PODANTIAFFINITY_TOPOLOGY_KEY                | Prometheus pod antiaffinity topology key                                                                                                                                                      | false    |                                                              |
| AVALOQ_PROMETHEUS_DATABASE_RETENTION_TIME                     | The length of time Prometheus will keep individual metrics                                                                                                                                    | false    | 14d                                                          |
| AVALOQ_PROMETHEUS_NODE_SELECTOR_KEY                           |                                                                                                                                                                                               | false    | dummySelector                                                |
| AVALOQ_PROMETHEUS_NODE_SELECTOR_VALUE                         |                                                                                                                                                                                               | false    | true                                                         |
| AVALOQ_PROMETHEUS_VOLUME_HOSTPATH_DATA                        | Prometheus hostpath for data                                                                                                                                                                  | false    |                                                              |
| AVALOQ_PROMETHEUS_PVC_STORAGE_REQUEST_DATA                    | Prometheus storage request for storing its database                                                                                                                                           | false    | 1Gi                                                          |
| AVALOQ_PROMETHEUS_PVC_STORAGE_CLASSNAME_DATA                  | Prometheus PersitentVolumeClaim data storage class name                                                                                                                                       | false    |                                                              |
| AVALOQ_PROMETHEUS_PVC_STORAGE_ACCESSMODE_DATA                 | Prometheus PersitentVolumeClaim data storage access mode                                                                                                                                      | false    | ReadWriteOnce                                                |
| AVALOQ_PROMETHEUS_SECURITYCONTEXT_PRIVILEGED                  |                                                                                                                                                                                               | false    | false                                                        |
| AVALOQ_PROMETHEUS_SECURITYCONTEXT_RUNASUSER                   | Prometheus prviledged user id                                                                                                                                                                 | false    |                                                              |
| AVALOQ_PROMETHEUS_RESOURCES_LIMIT_CPU                         | Prometheus CPU limit                                                                                                                                                                          | false    | 2000m                                                        |
| AVALOQ_PROMETHEUS_RESOURCES_REQUEST_CPU                       | Prometheus CPU request                                                                                                                                                                        | false    | 500m                                                         |
| AVALOQ_PROMETHEUS_RESOURCES_LIMIT_MEMORY                      | Prometheus memory limit                                                                                                                                                                       | false    | 2048Mi                                                       |
| AVALOQ_PROMETHEUS_RESOURCES_REQUEST_MEMORY                    | Prometheus memory request                                                                                                                                                                     | false    | 2048Mi                                                       |
| AVALOQ_PROMETHEUS_PROXY_RESOURCES_LIMIT_CPU                   | Prometheus Node exporter CPU limit                                                                                                                                                            | false    | 50m                                                          |
| AVALOQ_PROMETHEUS_PROXY_RESOURCES_REQUEST_CPU                 | Prometheus Node exporter CPU request                                                                                                                                                          | false    | 10m                                                          |
| AVALOQ_PROMETHEUS_PROXY_RESOURCES_LIMIT_MEMORY                | Prometheus Node exporter memory limit                                                                                                                                                         | false    | 256Mi                                                        |
| AVALOQ_PROMETHEUS_PROXY_RESOURCES_REQUEST_MEMORY              | Prometheus Node exporter memory request                                                                                                                                                       | false    | 256Mi                                                        |
| AVALOQ_PROMETHEUS_NODE_EXPORTER_CONTAINER_IMAGE               | Container image of Prometheus Node exporter                                                                                                                                                   | false    | openshift3/prometheus-node-exporter:v3.11.465                |
| AVALOQ_PROMETHEUS_NODE_EXPORTER_PORT                          |                                                                                                                                                                                               | false    | 9100                                                         |
| AVALOQ_PROMETHEUS_NODE_EXPORTER_RESOURCES_REQUEST_CPU         |                                                                                                                                                                                               | false    | 100m                                                         |
| AVALOQ_PROMETHEUS_NODE_EXPORTER_RESOURCES_LIMIT_MEMORY        |                                                                                                                                                                                               | false    | 64Mi                                                         |
| AVALOQ_PROMETHEUS_NODE_EXPORTER_RESOURCES_REQUEST_MEMORY      |                                                                                                                                                                                               | false    | 32Mi                                                         |
| AVALOQ_PROMETHEUS_NODE_EXPORTER_RESOURCES_LIMIT_CPU           |                                                                                                                                                                                               | false    | 200m                                                         |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_CONTAINER_IMAGE            | Container image of Prometheus Rule Provisioner                                                                                                                                                | false    | avaloq/avaloq-prometheus-rule-provisioner:0.2.4              |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_PROMETHEUS_USERNAME        | Username used by Prometheus Rule Provisioner to access Prometheus                                                                                                                             | false    |                                                              |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_PROMETHEUS_PASSWORD        | Password used by Prometheus Rule Provisioner to access Prometheus                                                                                                                             | false    |                                                              |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_PROMETHEUS_CERT_PATH       | Path to certificate used by Prometheus Rule Provisioner to serve encrypted connections                                                                                                        | false    | /var/run/secrets/kubernetes.io/serviceaccount/service-ca.crt |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_REPLICAS                   | Number of replicas of Prometheus Rule Provisioner                                                                                                                                             | false    | 1                                                            |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_NODE_SELECTOR_VALUE        | Specify a node where Prometheus Rule Provisioner is deployed                                                                                                                                  | false    | true                                                         |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_SECURITYCONTEXT_PRIVILEGED | Run Prometheus Rule Provisioner as privileged pods                                                                                                                                            | false    | false                                                        |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_SECURITYCONTEXT_RUNASUSER  | Prometheus Rule Provisioner security context run as user                                                                                                                                      | false    |                                                              |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_RESOURCES_REQUEST_CPU      | Prometheus Rule Provisioner CPU request                                                                                                                                                       | false    | 25m                                                          |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_RESOURCES_LIMIT_MEMORY     | Prometheus Rule Provisioner memory limit                                                                                                                                                      | false    | 512Mi                                                        |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_RESOURCES_REQUEST_MEMORY   | Prometheus Rule Provisioner memory request                                                                                                                                                    | false    | 512Mi                                                        |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_RESOURCES_LIMIT_CPU        | Prometheus Rule Provisioner CPU limit                                                                                                                                                         | false    | 200m                                                         |
| AVALOQ_PROMETHEUS_RULE_PROVISIONER_LOGGING_LEVELS             | Comma-separated list of custom logging levels per logger. Logger names must be written in snake_case, logging levels as defined by log4j2. Example: "LOGGING_LEVEL=WARN,ORG_THIRDPARTY=ERROR" | false    | LOGGING_LEVEL=info                                           |

# AvaloqFiles

| Name                                                       | Description | Required | Default value                                                                                          |
|------------------------------------------------------------|-------------|----------|--------------------------------------------------------------------------------------------------------|
| prometheus-configuration/prometheus-configuration.yml      |             | false    |                                                                                                        |
| prometheus-configuration/prometheus-configuration-ocp4.yml |             | false    |                                                                                                        |
| prometheus-configuration/htpasswd                          |             | false    | [htpasswd](../../../output/definitions/com.avaloq/avaloq-prometheus/prometheus-configuration/htpasswd) |
| etcd-certificates/etcd-ca-certificate                      |             | false    |                                                                                                        |
| etcd-certificates/etcd-certificate                         |             | false    |                                                                                                        |
| etcd-certificates/etcd-key                                 |             | false    |                                                                                                        |

**Note:** The default values for AvaloqFiles (if any) are present after running the `fetch` command.