# ansible_lihas_apache
Installs haproxy and does basic configuration, can use lihas_dehydrated with lihas_apache to request letsencrpt ssl certificates

* local_pages: Makro to direct a domain to a local document root
* external_redirect_domains: Makro to redirect a domain to some other domain
* reverse_proxy: Makro to create reverse proxy for a domain

To run solo:
```
ansible-galaxy install -r requirements.yml
ansible-playbook -i localhost, haproxy.yml
```
## Role Variables
```
%.config.roles.haproxy.http.DOMAINNAME
  target_ip: IP of real host, will de added to /etc/hosts as IP DOMAINNAME
```
