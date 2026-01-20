# Nerd Font Installer (`inf`)

`inf` is a simple command-line tool to download and install fonts from [Nerd Fonts](https://nerdfonts.com) directly to your Linux system.

## Installation

1. **Clone this repository** (or download the `inf` script):

```bash
git clone https://github.com/uberbl4tt/nerd-font-installer.git
cd nerd-font-installer
````

2. **Make the script executable**:

```bash
chmod +x inf
```

3. **Move it to a folder in your PATH** (optional, so you can run it anywhere):

```bash
sudo mv inf /usr/local/bin/
```



## Usage

Install a font by name:

```bash
inf <fontname>
```

**Example:**

```bash
inf FiraCode
```

This will:

1. Download the font from Nerd Fonts releases (default version `v3.4.0`)
2. Unpack it into `~/.local/share/fonts/nerd-fonts/<FontName>`
3. Update your system’s font cache
4. Clean up temporary files

> If no font name is provided, `inf` will print usage instructions.



## Notes

* The script expects **Linux** with `wget`, `unzip`, and `fc-cache` installed.
* Installed fonts go to `~/.local/share/fonts/nerd-fonts` by default.
* Check [Nerd Fonts](https://www.nerdfonts.com/font-downloads) if a font is not found.

## Finding the Right Font Name

Sometimes the name on the [Nerd Fonts Website](https://www.nerdfonts.com/font-downloads) is slightly different from the filename stored on GitHub. If a font fails to download, it’s usually because the ZIP file has a specific internal name.

**Example:**

* **Website Name:** Hasklug Nerd Font
* **Actual ZIP Name:** `Hasklig.zip`
* **Command:** `inf Hasklig`

### How to check the "Real" name:

1. Go to the [Nerd Fonts Downloads](https://www.nerdfonts.com/font-downloads) page.
2. Hover over the **Download** button for your font.
3. Look at the URL at the bottom of your browser or click it to see the ZIP name.
4. Use the **exact name** of that ZIP file (without the `.zip`) in your command!

> [!TIP]
> The script is CaSE sENsITIVE!!!!!.
> Also, double check the download link, some fonts may have a different font name on the download link.



## Example Run

```bash
$ inf FiraCode
searching for the shinies... ( •̀ω•́ )✧
unpacking the magic font box... 📦
telling the system about your cool new look... 🗣️
your font is installed and ready to use! ٩(^ᗜ^ )و ´-
```
