# Ansible Role: Letsencrypt

Installs [Letsencrypt](https://letsencrypt.org/) on Debian/Ubuntu.

## Role Variables

    letsencrypt_email: admin@{{ ansible_hostname }}

Email used on Letsencrypt registration.

    letsencrypt_rsa_size: 4096

RSA Key size (letsencrypt default is 2048)

    letsencrypt_domains: []

Domains (array of domain and webroot)

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - role: pabloguerino.letsencrypt
          letsencrypt_domains:
            - domains: "example.com,www.example.com"
              webroot: "/var/www/example.com"
            - domains: "example.org,www.example.org"
              webroot: "/var/www/example.org"


## License

MIT / BSD

## Author Information

This role was created in 2016 by [Pablo Guerino](https://github.com/pabloguerino)