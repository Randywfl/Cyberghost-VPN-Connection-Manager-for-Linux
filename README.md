# Cyberghost-VPN-Connection-Manager-for-Linux
Cyberghost VPN Connection Manager for Linux
Origin nand dependencies:

Written and compiled usng PureBasic 6.40 for my personal use on Debian 13.5 w/Xfce
Runtime dependencies are as follows: (must be present when running the compiled app):

cyberghostvpn — the actual CLI binary being controlled, expected at /usr/bin/cyberghostvpn

sudo — with the passwordless rule you set up in /etc/sudoers.d/cyberghost scoped to that one binary

openvpn — CyberGhost's OpenVPN backend (installed automatically during CyberGhost's own install)

wireguard / wireguard-tools — also pulled in by CyberGhost's installer, used if you ever switch to the WireGuard service type

curl — used by the IP/location check, hitting https://ipinfo.io/json

Internet access to ipinfo.io for that same check

~/cyberghost_cities.txt — the external data file for populating cities; app still runs without it, just with no per-country city lists

DejaVu Sans font (or a fallback) — used for the larger UI text; if missing, LoadFont() just fails quietly and the app falls back to the default system font, no crash
GTK — the underlying Linux GUI toolkit PureBasic builds against on Debian; this is normally already present on any XFCE/GNOME desktop
