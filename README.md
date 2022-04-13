Ansible Role: pi-led
=========

Create a service to disable/enable power and activity led on a raspberry pi

Requirements
------------

A Raspberry Pi (1B, 2B, 3B, 3B+, 4B) running Raspberry Pi OS

Role Variables
--------------

`create_service` creates the service to persist when raspberry pi is rebooted
`disable_power_led` if set to true, power led will be disabled disable default: true
`disable_activity_led` if set to true, activity led will be disabled default: false

`power_led` defines the led for the power led. default: "led0"
`activity_led` defines the led for the activity led. default: "led1"

Dependencies
------------

This role uses the set_fact, slurp, systemd, and the template module.

Example Playbook
----------------

    - hosts: rasbperrypi
      roles:
         - role: pi-led

License
-------

MIT

Author Information
------------------

[Jeff Swindel](https://jeffswindel.blogspot.com/)
