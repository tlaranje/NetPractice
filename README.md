*This project has been created as part of the 42 curriculum by <tlaranje\>.*

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
- Use **[Get my config]** to export your solution for that level — do this before moving to the next level.
- Once a level is complete, click **[Next level]** to continue.

### Exporting and submitting

After completing each level, export the configuration file using the **Get my config** button before moving on. You must submit **10 configuration files** (one per level), placed at the **root of your Git repository**.

Do not forget to enter your login in the interface before exporting — the files must be generated with your login.

During the peer-evaluation defense, you will be asked to complete 3 random levels under a time limit. External tools are not allowed; a simple calculator (e.g., `bc`) is the only exception.

## Resources

### Networking concepts studied

- **TCP/IP addressing** — how IP addresses are structured and assigned to network interfaces
- **Subnet masks** — how masks define the network and host portions of an address, in dotted-decimal and CIDR notation (e.g. `/24`)
- **Default gateways** — the router interface a host uses to forward packets outside its local subnet
- **Routing tables** — how routers and hosts decide where to forward packets, using route matching and next-hop gateways
- **Routers** — devices that connect different networks and forward packets between them based on routing tables
- **Switches** — devices that connect multiple hosts within the same network at the data-link layer
- **OSI model layers** — understanding which layer handles addressing (Layer 3 — Network), switching (Layer 2 — Data Link), and physical transmission (Layer 1)

### References

- [NetPractice Guide by lpaube — GitHub](https://github.com/lpaube/NetPractice)
- [Cisco — Understanding IP Addressing and Subnetting](https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html)
- [Subnet Calculator](https://www.subnet-calculator.com/)
- [Khan Academy — How the Internet Works](https://www.khanacademy.org/computing/computers-and-internet)
- [RFC 791 — Internet Protocol specification](https://datatracker.ietf.org/doc/html/rfc791)
- [Wikipedia — OSI model](https://en.wikipedia.org/wiki/OSI_model)
- [Wikipedia — Classless Inter-Domain Routing (CIDR)](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)

### AI usage

AI (Claude by Anthropic) was used during this project for the following tasks:

- **Understanding concepts**: clarifying how subnet mask calculations work, how routing tables are evaluated (first-match logic), and how default gateways interact with routing
- **Debugging**: asking targeted questions when a level's logs showed errors like "destination does not match any route" or "packet not for me"
- **README**: generating the initial draft of this README, which was then reviewed, corrected, and adapted to match the actual project

All AI-generated content was verified against the NetPractice simulation and official documentation before being accepted.