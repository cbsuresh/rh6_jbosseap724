# rh6_jbosseap724

Instructions to install JBOSS EAP 7.2 on RHEL 6.x servers. Cumulative Patch of JBOSS EAP 7.2.4 is applied to remediate the latest security vulnerabilities.

Addresses the latest CVEs as below:

CVE-2019-14838 wildfly-core: Incorrect privileges for 'Monitor', 'Auditor' and 'Deployer' user by default

CVE-2019-14843 wildfly: wildfly-security-manager: security manager authorization bypass

wget the required silent installation files from Artifactory.

cd /tmp

wget http://artifactory/artifactory/application-release-local/gov/usda/fs/jboss-eap/rhel6_jboss_eap_7.2.4_install.tar.gz

sha256sum rhel6_jboss_eap_7.2.4_install.tar.gz

Expected results: 276a4dcd8dca0b6ba792c8c68b0c31a6a4e553e0cecab210734149edef202006 ./rhel6_jboss_eap_7.2.4_install.tar.gz

tar xvzf rhel6_jboss_eap_7.2.4_install.tar.gz; echo Exit code is $?.

cd /tmp/jbosseap724

./install_rhel6_jboss_eap_7.2.4.sh -install
