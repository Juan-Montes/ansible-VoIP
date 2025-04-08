# Ansible for Telephony VoIP
![image](https://github.com/user-attachments/assets/f7043167-7d36-431a-a72b-9b5a211aab44)

## Playbook upload_agenda.yml

The upload of the agenda in the different Voip Endpoints is difficult as the amount of these increases. To expedite an efficient and rapid process for the maintenance of the telephone agenda, you can program a playbook in anxious to do this work in a group of host that we have in our inventory.

To run the playbook on the command line, simply execute:

```[admin@localhost playbooks]# ansible-playbook uploadagendaGXP.yml ```

This playbook example is designed for GrandStream VoIP terminals, which update the phonebook via HTTP.

The Burpsuite tool was used to capture GET/POST requests made to the HTTP API on the phones and schedule these requests in our playbook.

![imagen](https://github.com/user-attachments/assets/2d224cd5-3b8a-446f-b0bf-293584225827)


Thanks to this Burpsuite reverse proxy, we were able to successfully test the automated deployment of the phonebook.

## Playbooks timeZoneDate.ym & changepasswd.yml

The same methodology was used to create the other two playbooks, called "timeZoneDate.yml" and "changepasswd.yml," which are used to modify the VoIP phone's time zone and change the HTTP API admin password, respectively.
