# 🐕 FidruaFeast

**Samoyed Resource Muncher** - Let Fidrua munch your idle VPS resources!

```
                                   __   __
                                  /  \_/  \
    .---------------.            (  o   o  )
    | [*]  :::::::: |_ _ _ _ _ _ _/    V    \
    | ============= |____________(  \___/  )
    |_______________|              \_______/
```

## What is this?

FidruaFeast is a resource consumer tool that keeps your VPS alive by consuming idle CPU, memory, and disk resources. When your system needs resources back, Fidrua will spit them out!

## Features

- 🦴 **CPU Control** - Consume idle CPU cycles
- 🦴 **Memory Control** - Allocate unused memory
- 🦴 **Disk Control** - Fill up unused disk space
- 🐕 **Auto-adjust** - Automatically release resources when needed
- 📊 **Live Status** - Watch Fidrua eat in real-time
- 🏠 **Systemd Service** - Run as a background service

## Installation

### Download Binary

```bash
# Download latest release
wget https://github.com/donma033x/fidruafeast/releases/latest/download/fidruafeast-linux-amd64.tar.gz
tar -xzf fidruafeast-linux-amd64.tar.gz
chmod +x fidruafeast

# Install as service
sudo ./fidruafeast -install
```

### Build from Source

```bash
git clone https://github.com/donma033x/fidruafeast.git
cd fidruafeast
go build -o fidruafeast main.go
```

## Usage

```bash
# Show help
fidruafeast -h

# Run with defaults (keep 45% free)
fidruafeast

# Custom targets
fidruafeast -cpu 30 -mem 20 -disk 40

# Run in background
fidruafeast -daemon

# Check status
fidruafeast -status

# Install as systemd service
sudo fidruafeast -install

# Uninstall service
sudo fidruafeast -uninstall
```

## Options

| Option | Description | Default |
|--------|-------------|---------|
| `-cpu` | Keep this % CPU free | 45 |
| `-mem` | Keep this % Memory free | 45 |
| `-disk` | Keep this % Disk free | 45 |
| `-daemon` | Run in background mode | false |
| `-status` | Watch Fidrua's status | - |
| `-install` | Adopt Fidrua (systemd) | - |
| `-uninstall` | Release Fidrua | - |

## Why "Fidrua"?

Fidrua is a Samoyed 🐕 who loves to munch on things. In this case, he munches on your idle server resources!

## License

MIT License
