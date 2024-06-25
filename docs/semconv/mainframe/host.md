# Resource host - host.id and host.name mapping

The [resource host](https://opentelemetry.io/docs/specs/semconv/attributes-registry/host/) defines the ``host.id`` as a unique host ID and the ``host.name`` as the name of the host.

The ``host.id`` is in Cloud environment the ``instance_id`` of the cloud provider. For non-containerized system, it should be the ``machine-id``. Source of ``machine-id`` varies by operating system.

The ``host.name`` is either the output of the hostname command, the full qualiefied hostname (FQDN) or a name specified by the users.

The attribute [``deployment.environment``](https://opentelemetry.io/docs/specs/semconv/attributes-registry/deployment/) provides the name of the deployment environment, e.g., staging or production. The attribute is to be set in mainframe environments when host.id or host.name are only unique within a deployment environment. 


| Resource | source (API or command) | host.id | host.name |
|----|----|----|----|
| LPAR | IBM Z HMC API | object-id, e.g., d6641179-b8e0-3980-9d22-32cdd967c774 | name, e.g., VM137 |
| LPAR or VM | 3rd party management software | uuid | name or FQDN |
| z/OS LPAR or VM | ``d xcf`` | Combination of sysplex name (8 chars) and SMFID (4 chars), e.g., ``SYSPLEX1-SYSID`` | SMFID (4 chars), e.g., ``SYS1`` | 
| Linux LPAR | ``hostname --fqdn``| | FQDN |
| TPF LPAR or VM | |  | Combination of system name, complex name,  and environment, e.g., ``TPFA-RES-PROD``| 
| z/VM LPAR | | | ``SYSTEMID`` or FQDN  |
| VMs on z/VM | ``query users`` <br>``hostname --fqdn``| userid | FQDN |
| VMs on KVM | ``virsh list`` <br>``hostname --fqdn`` | domain name | FQDN | 



