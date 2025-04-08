# 🌍 IP Geolocation Lookup Tool

A Python script to fetch geolocation information for multiple IP addresses from a file using the [ipinfo.io](https://ipinfo.io) API.

## ✨ Features

- 📂 Reads IP addresses from a file (one per line or comma-separated)
- 🔍 Fetches geolocation data including:
  - 📡 IP address
  - 🏷️ Hostname
  - 🏙 City
  - 🗺️ Region
  - 🇺🇳 Country
  - 📍 Location coordinates
  - 🏢 Organization
- 🌈 Color-coded output for better readability
- ⚠️ Handles errors gracefully

## 📋 Requirements

- Python 3.x
- `requests` library
- `colorama` library

## 🔧 Installation

1. Clone the repository or download the script
2. Install the required dependencies:

```bash
pip install requests colorama

🚀 Usage
bash
Copy

python ip_geolocation.py --file <path_to_file>

📝 Input File Format

The input file can contain IP addresses in either format:

    One IP per line

    Comma-separated list of IPs

Example:
Copy

8.8.8.8
1.1.1.1

or
Copy

8.8.8.8, 1.1.1.1

💻 Example Output
json
Copy

{
    "ip": "8.8.8.8",
    "hostname": "dns.google",
    "city": "Mountain View",
    "region": "California",
    "country": "US",
    "loc": "37.4056,-122.0775",
    "org": "AS15169 Google LLC"
}

ℹ️ API Notes

This script uses the free tier of ipinfo.io API, which has some limitations:

    ⏱️ 50,000 requests per month

    🚦 Rate limiting may apply

    🔓 No authentication required for free tier

For heavy usage, consider getting an API token from ipinfo.io
📜 License

This project is open-source and available under the MIT License.
Copy


You can save this as `README.md` or download it directly if hosted. The emojis make the document more engaging and help visually separate different sections. Would you like me to make any adjustments to the emoji selection or add more visual elements?

You can save this as `README.md`

Here's the final README.md file with emojis, ready to save to your project:
markdown
Copy

# 🌍 IP Geolocation Lookup Tool

A Python script to fetch geolocation information for multiple IP addresses using the [ipinfo.io](https://ipinfo.io) API.

## ✨ Features

- 📂 Read IPs from file (one per line or comma-separated)
- 🔍 Fetch geolocation data including:
  - 📡 IP address
  - 🏷️ Hostname
  - 🏙️ City
  - 🗺️ Region
  - 🇺🇳 Country
  - 📍 GPS coordinates
  - 🏢 Organization/ISP
- 🌈 Color-coded console output
- ⚠️ Error handling
- 🚀 Fast batch processing

## 📋 Requirements

- Python 3.6+
- `requests` library
- `colorama` library

## 🔧 Installation

```bash
pip install requests colorama

🚀 Usage
bash
Copy

python ip_geolocation.py --file ips.txt

📝 Input File Example

ips.txt:
Copy

8.8.8.8
1.1.1.1
2606:4700:4700::1111

💻 Sample Output
json
Copy

{
    "ip": "8.8.8.8",
    "hostname": "dns.google",
    "city": "Mountain View",
    "region": "California",
    "country": "US",
    "loc": "37.4056,-122.0775",
    "org": "AS15169 Google LLC",
    "postal": "94043",
    "timezone": "America/Los_Angeles"
}

⚙️ Configuration

For higher request limits:

    Get free token at ipinfo.io

    Modify script to add:
    python
    Copy

    headers = {'Authorization': f'Bearer YOUR_TOKEN'}
    response = requests.get(url, headers=headers)

📜 License

MIT License - Free for personal and commercial use
