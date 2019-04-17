# osp_health_checks
A basic set of openstack health check commands in a simple ansible playbook. Conterized playbook has docker based service checks and applies to osp 12/13 and later. Non containerized for OSP 11 and earlier.
First create an ansible inventory , ex, hosts and run the playbooks by ansible-playbook containerized.yaml -v

[controllers]

172.16.6.7

172.16.6.14

172.16.6.10

[computes]

172.16.6.13

172.16.6.12

172.16.6.20

This was devloped to run from Red Hat OSP director as it takes care of ssh key based authentication to controlelrs and computes. This assumes you correctly add the controllers in order in to the ansible inventory as controller[0] is hardcoded in to some health checks and it expects the docker contaner bundles to be in the format rabbitmq-bundle-0 etc..Also the rc file location is hardcoded.


