### 3.0.1

- Fixed failing ca.crt reuse from open-source Puppet

### 3.0.0

- Added support for multisite indexer clustering
- Added replication_port parameter to configure index cluster replication port.
- Moved useACK paramter to use_ack due to [Puppet stricter language check](https://docs.puppet.com/puppet/latest/reference/lang_reserved.html#parameters)

### 2.1.2

- Improved SAML support and updated settings for Splunk 6.4 and Splunk 6.5

### 2.1.1

- Improved search head clustering (SHC) support: Puppet now only places the initial SHC node configuration, and won't touch it afterwards. This allows the SH deployer to take over after initial configuration. A staging SHC instance is no longer necessary.
- Improved search head clustering (SHC) support: `splunk init shcluster` is no longer necessary, only `splunk bootstrap shcluster-captain`

### 2.1.0

- Added search head clustering (SHC) support, although only useful for staging purposes due to the overruling nature of the search head deployer (SHD)
- Added support to reuse Puppet certs from /etc/puppetlabs/puppet/ssl whenever commercial Puppet is used.

### 2.0.0

- Moved Splunk configuration out of etc/system/local to individual Splunk config apps
- Add LDAP authentication support 

### 1.0.9

- Added phonehomeintervalinsec parameter to configure phoneHomeIntervalInSec for the deploymentclient

### 1.0.8

- Improved adding search peers
- Added class containment, to properly support `require =>` from other resources or classes. This add a dependency on puppetlabs-stdlib.

### 1.0.7

- Added rpsec tests
- Added github->travis-ci integration
- Fixed issues for Puppet 2.7

### 1.0.6

- Add SAML authentication support through ADFS as IdP

### 1.0.5

- Specify IP to bind to

### 1.0.4

- Optionally specify Splunk version to install
- Merged PR #1 from @timidri

### 1.0.3

- Added `ds_intermediate` parameter to create a deployment server that can deploy apps from an another upstream deployment server.

### 1.0.2

- Added `use_ack` parameter to manage indexer acknowledgement
- Updated README with Debian / Ubuntu prerequisites.

### 1.0.1

- Added `service` parameter to manage start and running state of the Splunk or Splunkforwarder service.

### 1.0.0

Initial release: 

- License master
- Splunk web
- Standalone search head
- KVstore
- Standalone indexer
- Deployment server
- Deployment client
- Distributed search
- Forwarding with load-balancing
- Data input with SSL
- Index clustering: cluster master
- Index clustering: cluster peer
- Index clustering: search head