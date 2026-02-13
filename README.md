# Visual Subnet Calculator

A web-based tool for calculating and visualizing IPv4 subnet divisions. This interactive calculator allows network administrators to split and join subnets dynamically, with a visual tree representation of the subnet hierarchy.

## Acknowledgment

This tool is based upon the original [Visual Subnet Calculator](https://www.davidc.net/sites/default/subnets/subnets.html) by DavidC. I liked the original so much that I decided to add more features to it.

## Live Demo

Access the tool at: https://midnightflux.github.io/subnet-calculator/

## Features

- **Visual Subnet Splitting**: Click to divide subnets into smaller chunks
- **Subnet Joining**: Click on parent subnet boundaries to merge child subnets
- **Real-time Calculations**: Automatically calculates address ranges, usable IPs, and host counts
- **Customizable Columns**: Toggle visibility for different information columns
- **Reserve IPs**: Configure reserved IPs at the beginning and end of each subnet
- **Remarks**: Add custom notes to each subnet for documentation
- **Bookmarkable State**: Save and share your subnet configurations via URL

## Usage

1. Open `index.html` in any modern web browser
2. Enter your network address (e.g., `192.168.0.0`)
3. Enter the CIDR mask bits (e.g., `16` for `/16`)
4. Click **Update** to generate the initial subnet table
5. Use **Divide** to split a subnet into two smaller subnets
6. Use the **Join** columns to merge subnets back together
7. Adjust **Reserve IPs** if needed (default reserves network and broadcast addresses)
8. Add **Remarks** to document subnet purposes
9. Bookmark the link to save your configuration

## Column Options

| Column | Description |
|--------|-------------|
| Subnet address | CIDR notation of the subnet (e.g., 192.168.1.0/24) |
| Netmask | Dotted decimal netmask (e.g., 255.255.255.0) |
| Range of addresses | Full IP range of the subnet |
| Useable IPs | Range excluding reserved addresses |
| Hosts | Number of usable host addresses |
| Remark | Custom notes for the subnet |
| Divide | Action to split the subnet |
| Join | Action to merge with sibling subnet |

## Technical Details

- Pure HTML/CSS/JavaScript - no server required
- Binary tree data structure for subnet hierarchy
- URL-based state serialization for sharing configurations

## Browser Compatibility

Works with all modern browsers:
- Chrome
- Firefox
- Safari
- Edge

## Project Structure

```
subnet-calculator/
├── index.html      # Main application entry point
├── css/
│   └── style.css   # Styling
├── js/
│   └── app.js      # Core application logic
└── README.md       # This file
```

## License

MIT License - feel free to use and modify as needed.
