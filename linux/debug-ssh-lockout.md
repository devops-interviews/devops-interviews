# Debug SSH Lockout

> **Company:** TCS | **Difficulty:** Medium

---

#### **Scenario**

The developer account **dev** has been locked out of the server. Security logs indicate the SSH daemon's **authentication failure limit** was triggered.

#### **Task**

Check the logs to count exactly how many times the user failed `today`. Update the SSH configuration to increase the allowed login attempts `above that number`.

#### **Example**

```
root@server:~# tail /var/log/auth.log
Dec 23 09:12:01 server sshd[2201]: Failed password for dev from 10.0.0.5 port 5432 ssh2
Dec 23 09:12:05 server sshd[2201]: Failed password for dev from 10.0.0.5 port 5432 ssh2
Dec 23 09:12:08 server sshd[2201]: Failed password for dev from 10.0.0.5 port 5432 ssh2

```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/debug-ssh-lockout)
