# Cool Desktop Wallpapers

A collection of AI-generated desktop wallpapers in the style of Hiroshi Nagai.

## About

These wallpapers were created using **Midjourney** with prompts describing historical cities and locations rendered in the distinctive style of Hiroshi Nagai - known for his dreamy, nostalgic Japanese citypop aesthetic featuring clean lines, vibrant colors, and serene summer vibes.

## Wallpapers

| Name | Description |
|------|-------------|
| `cajamarca.png` | Cajamarca, Peru circa 1500s |
| `potosi.png` | Potosí, Bolivia circa 1650 |
| `seville.png` | Seville, Spain circa 1509 |
| `tenochtitlan-1.png` - `tenochtitlan-4.png` | Tenochtitlan, Aztec Empire |
| `temple-1.png` - `temple-2.png` | The First Temple of Jerusalem |

## Resolution

Most images are high resolution, suitable for 4K-6K displays.

## Usage

Feel free to use these as desktop wallpapers for personal use.

## Hyprland Auto-Rotation Setup

To automatically rotate through these wallpapers every 2 hours in Hyprland (using `swww`):

```bash
# Clone the repo
git clone https://github.com/Dicklesworthstone/cool_desktop_wallpapers.git ~/Pictures/Wallpapers

# Create rotation script
cat > ~/Pictures/Wallpapers/rotate.sh << 'EOF'
#!/bin/bash
WALLPAPER_DIR="$HOME/Pictures/Wallpapers"
WALLPAPER=$(find "$WALLPAPER_DIR" -type f \( -name "*.png" -o -name "*.jpg" \) | shuf -n 1)
swww img "$WALLPAPER" --transition-type grow --transition-duration 2
EOF
chmod +x ~/Pictures/Wallpapers/rotate.sh

# Create systemd user service
mkdir -p ~/.config/systemd/user
cat > ~/.config/systemd/user/wallpaper-rotate.service << 'EOF'
[Unit]
Description=Rotate wallpaper

[Service]
Type=oneshot
ExecStart=%h/Pictures/Wallpapers/rotate.sh
EOF

# Create timer (runs every 2 hours)
cat > ~/.config/systemd/user/wallpaper-rotate.timer << 'EOF'
[Unit]
Description=Rotate wallpaper every 2 hours

[Timer]
OnBootSec=5min
OnUnitActiveSec=2h
Persistent=true

[Install]
WantedBy=timers.target
EOF

# Enable and start
systemctl --user daemon-reload
systemctl --user enable --now wallpaper-rotate.timer

# Change wallpaper now
~/Pictures/Wallpapers/rotate.sh
```

## License

These AI-generated images are shared freely. Attribution appreciated but not required.
