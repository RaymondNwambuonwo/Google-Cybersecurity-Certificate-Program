# Install software in a Linux distribution

## This lab consists of doing some installing and removing of packages via the command line.

### Scenario

Your role as a security analyst requires that you have the Suricata and tcpdump network security applications installed on your system.

In this scenario, you have to install, uninstall, and reinstall these applications on your Linux Bash shell. You also need to confirm that you’ve installed them correctly.

Here’s how you'll do this: First, you’ll confirm that APT is installed on your Linux Bash shell. Next, you’ll use APT to install the Suricata application and confirm that it is installed. Then, you’ll uninstall the Suricata application and confirm this as well. Next, you’ll install the tcpdump application and list the applications currently installed. Finally, you’ll reinstall the Suricata application and confirm that both applications are installed.

```bash
apt

sudo apt install suricata

Note: The apt install and apt remove commands must be prefixed with the sudo command as elevated privileges are required to install and uninstall software in Linux.

The Suricata application can take a few minutes to install.

    When you install an application with APT, the output displays details of all the software to be installed. This may include additional applications that depend on the new software. These additional applications are called the dependencies of the software to be installed.

suricata

sudo apt remove suricata

Suricata, a network analysis tool used for intrusion detection
tcpdump application. This is a command-line tool that can be used to capture network traffic in a Linux Bash shell

sudo apt install tcpdump

apt list --installed
list all installed apps

```
