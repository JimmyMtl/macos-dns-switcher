# 🛜🍎 macOS DNS Switcher (Python)

A command-line utility to programmatically change the DNS settings of your macOS network services using Python and
`networksetup`. It is based on [Yggland datas](https://yggland.fr/FAQ-Tutos/).

---

## ✨ Features

- Choose from pre-configured public DNS providers:
    - **OpenDNS**
    - **Cloudflare**
    - **Quad9**
    - Or reset to **default**
- Supports both **IPv4** and **IPv6** addresses
- Configure one or multiple **network services** (e.g., `Wi-Fi`, `Ethernet`, `iPhone USB`)
- Easily reset DNS to DHCP-provided values

---

## 🛠 Requirements

- macOS
- Python 3.x
- Admin privileges (`sudo` required to change network settings)

---

## 🚀 Installation

Clone the project:

```bash
git clone https://github.com/yourusername/mac-dns-switcher.git
cd mac-dns-switcher
```

## ▶️ Usage

Run the script with administrator privileges:

```bash
sudo python ./src/main.py
```

## 🧭 Interactive Menu

1. Select one or more network services (e.g., Wi-Fi, Ethernet)

2. Choose a DNS provider:
    - 0 – Default (reset DNS to DHCP)
    - 1 – OpenDNS
    - 2 – Cloudflare
    - 3 – Quad9

3. The script will apply the selected DNS settings to the chosen services.

## 🔍 Verifying DNS Settings

To check the DNS servers currently set on a network service, you can run:

```bash
networksetup -getdnsservers "Wi-Fi"
```

Replace `Wi-Fi` with the name of any other service you've configured.

## 🧼 Reset DNS to Default

To remove all custom DNS and return to DHCP-provided settings:

1. Run the script
2. Select your network service(s)
3. Choose option `0` (default) from the DNS provider list

## 🛡️ Notes & Warnings

- This script only works on macOS, using the built-in networksetup tool.

- It does not persist changes across different users or reboots unless the system is configured to retain them.

## 📄 License

MIT License

## 🙋 Support

Feel free to open an issue or submit a pull request if you’d like to contribute or request a feature!

---
