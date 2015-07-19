# Toran proxy with Vagrant & Ansible

Getting started an example/demo/personal usage of Toran Proxy - Packagist mirror

# Requirements

* vagrant

# Example Usage

1. Clone & Run `vagrant up`
2. Add host entry `192.168.33.100	toranproxy.local`
3. Navigate to `toranproxy.local` and follow it's setup instructions

If you wish to download the whole of Packagust's packges from GitHub for offline use, get a list from [Toran/Packagist Package list](https://github.com/eddiejaoude/toran-proxy-packages). Then update either via the web form on `toranproxy.local` or manually edit the yml config for the packages list in `toran/app/toran/config.yml`

---

# Known issues

A few people have had issues with CSRF token and Toran proxy setup form. The way to get around this is to turn off CSRF validation in the config.

Update `toran/app/config/config.yml` where **csrf_protection** with:

```yaml
framework:
    # ...
    csrf_protection: false
    # ...
```

Any questions raise an [issue here](https://github.com/eddiejaoude/toran-proxy-vagrant-ansible/issues).
