# Ansible_macaddrcli

Simple Ansible script to check vendor info for a device Mac Address.

- This script can be run locally or a remote host based on Inventory file.
- Ansible should be installed.
- Can use "XX:XX:XX:XX:XX:XX" OR "XX-XX-XX-XX-XX-XX" OR "XXXXXXXXXXXX" for Mac Address format.

## Usage

- Update your API Key as api_key variable on the script.

Then run the Script with a valid Mac Address:
```javascript
[ansible@ansibleCR ~]# ansible-playbook test.yml -e "macaddr=2C:54:91:88:C9:E3"
```
Output (vendor name):
```javascript
PLAY [Get MAC Adress vendor info] ************************************************************************************************************************************************************

TASK [Gathering Facts] ***********************************************************************************************************************************************************************
ok: [localhost]

TASK [Get API response] **********************************************************************************************************************************************************************
ok: [localhost]

TASK [debug] *********************************************************************************************************************************************************************************
ok: [localhost] => {
    "content.content": "Microsoft Corp"
}
```
