# Wrenone Pinner - Developer Documentation

## Tech Stack
- **Core**: Rust (window management)
- **GUI**: Python + PyQt5 (system tray and interface)
- **Build**: PyInstaller + Inno Setup

## Project Structure
```
window-pinner/
├── window_pinner_core/   # Rust core functionality
├── window_pinner.py      # Main Python application
├── build.ps1            # Build automation
└── installer.iss        # Installer configuration
```

## Setup Development Environment
1. Install requirements:
   - Rust (1.75+)
   - Python 3.13+
   - Visual Studio Build Tools
   - Inno Setup 6

2. Install dependencies:
```bash
pip install -r requirements.txt
cargo install maturin
```

## Building
1. Run build script:
```powershell
.\build.ps1
```
This will:
- Build Rust core
- Package Python application
- Create installer

## Key Components
1. **Rust Core**
   - Window handle management
   - Windows API integration
   - Process monitoring

2. **Python Layer**
   - System tray interface
   - Hotkey management
   - Settings persistence

3. **Build Pipeline**
   - Automated compilation
   - Resource bundling
   - Installer generation

## Testing
Run tests:
```bash
cargo test              # Rust tests
python -m pytest tests  # Python tests
```

## Contributing
1. Fork repository
2. Create feature branch
3. Make changes
4. Submit pull request

## Debug Tips
- Enable debug logs: Set `DEBUG=1` environment variable
- Use VSCode launch configurations in `.vscode/`
- Check build logs in `build/logs/`
