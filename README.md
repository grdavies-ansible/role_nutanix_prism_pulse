# Nutanix Role to configure Pulse on either Prism Element or Prism Central

This Ansible role downloads and deploys Nutanix Prism Central.


## Role Variables

| Variable                                     | Required | Default | Choices                   | Comments                                                                                               |
|----------------------------------------------|----------|---------|---------------------------|--------------------------------------------------------------------------------------------------------|
| role_nutanix_prism_pulse_host                | yes      |         |                           | The IP address or FQDN for the Prism (Element or Central) where you want to configure pulse.           |
| role_nutanix_prism_pulse_username            | no       | "admin" |                           | A valid username with appropriate rights to access the Nutanix API. where you want to configure pulse. |
| role_nutanix_prism_pulse_password            | yes      |         |                           | A valid password for the supplied username.  where you want to configure pulse.                        |
| role_nutanix_prism_pulse_port                | no       | 9440    |                           | The Prism TCP port  where you want to configure pulse.                                                 |
| role_nutanix_prism_pulse_validate_certs      | no       | false   | true / false              | Whether to check if Prism UI certificates are valid.                                                   |
| role_nutanix_prism_pulse_debug               | no       | false   | true / false              | Whether to output variable contents for debugging purposes.                                            |
| role_nutanix_prism_pulse_enable              | no       | true    | true / false              | True enables pulse. False disables pulse.                                                              |
| role_nutanix_prism_pulse_enable_email        | no       | false   | true / false              |                                                                                                        |
| role_nutanix_prism_pulse_email_contact_list  | no       | []      |                           |                                                                                                        |
| role_nutanix_prism_pulse_scrubbing_level     | no       | "AUTO"  |                           |                                                                                                        |
| role_nutanix_prism_pulse_prompt_needed       | no       | false   | true / false              |                                                                                                        |
| role_nutanix_prism_pulse_nos_version         | no       | null    |                           |                                                                                                        |
| role_nutanix_prism_pulse_remind_later        | no       | false   | true / false              |                                                                                                        |


## Dependencies

None


## Example Playbook

```
- hosts: localhost
  gather_facts: false
  roles:
    - role: grdavies.role_nutanix_prism_pulse
  vars:
    nutanix_host: 10.38.185.37
    nutanix_username: admin
    nutanix_password: nx2Tech165!
    role_nutanix_prism_pulse_status: True
```


## License

See LICENSE.md

## Author Information

Ross Davies
