# Ansible Collection - puppeteers.wordpress_misc

This collection includes configurations to apply before and after
[inmotionhosting.wordpress](https://galaxy.ansible.com/ui/standalone/roles/inmotionhosting/wordpress/)
role. That role is that it includes other dependency roles from meta/main.yml
in a predefined order (e.g. apache, nginx, php-fpm). This is problematic because those roles
depend on selinux rules set in the wordpress role, which gets run last.

# Roles

This collections includes two roles:

* *puppeteers.wordpress_misc.pre:* run before any of the dependencies of wordpress
* *puppeteers.wordpress_misc.post:* run before after wordpress (and its dependencies)
