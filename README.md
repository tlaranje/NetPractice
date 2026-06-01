*This project has been created as part of the 42 curriculum by \<tlaranje\>.*

# NetPractice

## Description

NetPractice is a practical networking exercise from the 42 curriculum. The goal is to configure 10 small-scale simulated networks so they function correctly. Through this project, you will learn how to assign IP addresses, configure subnet masks, set up default gateways, and understand how routers forward packets between networks.

The networks are entirely simulated and run locally in your web browser — no real network infrastructure is involved. Each level presents a broken network diagram that you must fix by modifying the available (unshaded) fields until the configuration is valid.

## Instructions

### Running the training interface

1. Download the project files from the project page.
2. Extract them into a folder of your choice.
3. Inside that folder, run the launch script:

```bash
bash run.sh
```

This will start a local web server and open the NetPractice interface in your default browser.

**If `run.sh` doesn't work**, you can start the server manually:
```bash
python3 -m http.server 49242
```
Then navigate to `http://localhost:49242` in your browser.

### Using the interface

- Enter your **intranet login** in the field on the main page before starting. This is required so the configuration files are tied to your account.
- Use the **Training** tab to practice with your personal configuration.
- Use the **Evaluation** tab to generate a random configuration (also valid for peer-evaluation).
- At each level, a non-functioning network diagram is shown. Modify the unshaded fields until the network works.
- Use **[Check again]** to verify your configuration.
- Use **[Get my config]** to export your solution for that level.
- Once a level is complete, click **[Next level]** to continue.

### Exporting and submitting

After completing each level, export the configuration file using the **Get my config** button before moving on. You must submit **10 configuration files** (one per level), placed at the **root of your Git repository**.

Do not forget to enter your login in the interface before exporting — the files must be generated with your login.

During the peer-evaluation defense, you will be asked to complete 3 random levels under a time limit. External tools are not allowed; a simple calculator (e.g., `bc`) is the only exception.

## Resources

### Networking concepts studied

- **TCP/IP addressing** — how IP addresses are structured and assigned to devices
- **Subnet masks** — how masks define the network and host portions of an address
- **CIDR notation** — shorthand representation of IP address + mask (e.g., `/24`)
- **Default gateways** — the router interface a host uses to reach addresses outside its subnet
- **Routing tables** — how routers and hosts decide where to forward packets
- **Routers and switches** — routers connect different networks; switches connect devices within the same network

### References

- [NetPractice Guide - GitHub repo by lpaube](https://github.com/lpaube/NetPractice)

### AI usage

AI was used during this project to:
- Help clarify networking concepts such as subnet mask calculations and routing table logic
- Double-check understanding of how default gateways and routes interact
- Help format this README.