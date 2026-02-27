# tmux config

> My personal tmux configuration — minimal, fast, and developer-friendly.
>
> Konfigurasi tmux pribadi — minimal, cepat, dan ramah untuk developer.

---

## Requirements / Kebutuhan

- `tmux >= 3.2`
- `git` (untuk auto-install TPM / for auto-installing TPM)
- `fzf` (untuk tmux-fzf / for tmux-fzf)
- `neovim` atau `vim` (opsional / optional)

Install fzf:
```bash
# Arch
sudo pacman -S fzf

# Ubuntu/Debian
sudo apt install fzf
```

---

## Installation / Instalasi

**1. Clone repository ini / Clone this repository**
```bash
git clone https://github.com/irfantrue/tmux-config ~/.config/tmux
```

**2. Beri permission pada install script / Give permission to install script**
```bash
chmod +x ~/.config/tmux/install-tpm.sh
```

**3. Jalankan tmux / Start tmux**
```bash
tmux
```

TPM akan otomatis terinstall saat tmux pertama kali dibuka.
TPM will be automatically installed when tmux is first opened.

**4. Install plugins**

Tekan / Press `Prefix + I` (kapital) untuk install semua plugin.

---

## Plugins

| Plugin | Fungsi / Function |
|--------|-------------------|
| [tpm](https://github.com/tmux-plugins/tpm) | Tmux Plugin Manager |
| [tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect) | Save & restore sessions |
| [tmux-continuum](https://github.com/tmux-plugins/tmux-continuum) | Auto-save sessions setiap 10 menit / every 10 minutes |
| [tmux-fzf](https://github.com/sainnhe/tmux-fzf) | Fuzzy finder untuk session, window, pane / for session, window, pane |

### tmux-resurrect
- Menyimpan dan merestore session tmux secara manual maupun otomatis
- Saves and restores tmux sessions manually or automatically
- File save disimpan di / Save files stored at: `~/.config/tmux/resurrect/`
- Maksimal 5 file save / Maximum 5 save files

### tmux-continuum
- Auto-save setiap 10 menit / Auto-save every 10 minutes
- Auto-restore saat tmux dibuka / Auto-restore when tmux starts

### tmux-fzf
- Fuzzy finder untuk navigasi session, window, dan pane
- Fuzzy finder for navigating sessions, windows, and panes

---

## Keybindings

> Prefix default: `Ctrl + Space` atau / or `Ctrl + b`

### General
| Keybind | Aksi / Action |
|---------|---------------|
| `Prefix + q` | Reload config |
| `Prefix + S` | Save session (manual) |
| `Prefix + L` | Restore session (manual) |
| `Prefix + f` | Buka tmux-fzf / Open tmux-fzf |

### Pane
| Keybind | Aksi / Action |
|---------|---------------|
| `Prefix + h` | Split horizontal (bawah / below) |
| `Prefix + v` | Split vertikal (kanan / right) |
| `Prefix + x` | Hapus pane / Kill pane |
| `Ctrl + Alt + ←↑↓→` | Navigasi pane / Navigate pane |
| `Ctrl + Alt + Shift + ←↑↓→` | Resize pane (5 unit) |

### Window
| Keybind | Aksi / Action |
|---------|---------------|
| `Prefix + c` | Window baru / New window |
| `Prefix + k` | Hapus window / Kill window |
| `Prefix + r` | Rename window |
| `Alt + 1-9` | Pindah ke window / Go to window 1-9 |

### Session
| Keybind | Aksi / Action |
|---------|---------------|
| `Prefix + C` | Session baru / New session |
| `Prefix + K` | Hapus session / Kill session |
| `Prefix + R` | Rename session |
| `Prefix + P` | Session sebelumnya / Previous session |
| `Prefix + N` | Session berikutnya / Next session |

### Copy Mode (Vi)
| Keybind | Aksi / Action |
|---------|---------------|
| `Prefix + [` | Masuk copy mode / Enter copy mode |
| `v` | Mulai seleksi / Begin selection |
| `y` | Copy dan keluar / Yank and exit |
| `Prefix + ]` | Paste |

---

## Structure / Struktur

```
~/.config/tmux/
├── tmux.conf          # Konfigurasi utama / Main config
├── install-tpm.sh     # Auto-install TPM
└── resurrect/         # File save session / Session save files
```

