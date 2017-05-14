# Ansible role: FreeBSD Common
This role which performs some simple tasks for deploying a FreeBSD system or jail.

# Tasks
## misc
Currently just enables the rc.conf variable clear_tmp_enable and the
net.inet.tcp.per_cpu_timers sysctl.
## pkg
Configures pkgng with custom repositories and installs specified public certificates.
### variables
**savagedlight_fbsdcommon_pkgng_certs** an array specifying the name of remote repositories public 
certificates to install.  
Example: If you add the value 'example.com', the file pkg/files/certs/hello.com.cert 
will be copied to /usr/local/etc/ssl/certs/hello.com.cert

**savagedlight_fbsdcommon_pkgng_repos** an array specifying repository configurations to install.  
Example: If you add the value 'hello.com-rproxy', the file pkg/files/repos/hello.com-proxy.conf 
will be copied to /usr/local/etc/pkg/repos/hello.com-proxy.conf

