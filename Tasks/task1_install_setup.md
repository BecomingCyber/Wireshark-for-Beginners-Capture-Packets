# Task 1: Install and Set Up Wireshark on Ubuntu

### 1.1 Install Wireshark on Ubuntu

To install the latest stable version of Wireshark, use the following command:

```bash
sudo add-apt-repository ppa:wireshark-dev/stable
sudo apt-get update
sudo apt-get install wireshark

1.2 Security Considerations
Wireshark should not be run as a superuser (root) due to security concerns. It’s recommended to configure the Wireshark group to allow non-root users to capture network packets.

1.3 Add Your User to the Wireshark Group
sudo usermod -aG wireshark $USER
This command adds your user account to the wireshark group, allowing you to capture packets without using superuser privileges. After running this command, log out and log back in to apply the changes.