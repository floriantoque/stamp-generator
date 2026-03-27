# stamp-generator

Generate rubber-stamp-style PNG images from the command line.

## Install & run

```bash
# From GitHub (no install needed)
uvx --from git+https://github.com/floriantoque/stamp-generator stamp-generator 'HELLO;WORLD'

# Or install locally
uv pip install git+https://github.com/floriantoque/stamp-generator
stamp-generator 'APPROVED' --color '#1E90FF'
```

## Usage

```bash
stamp-generator 'LINE 1;LINE 2' [OPTIONS]
```

### Options

| Flag | Default | Description |
|------|---------|-------------|
| `--rotation` | `12` | Angle in degrees |
| `--color` | `#FF2828` | Hex color of the stamp ink |
| `--noise` | `0.3` | Wear intensity: 0.0 (clean) to 1.0 (heavy) |
| `--output` | `stamp.png` | Output PNG file path |

### Examples

```bash
# Red stamp, default settings
stamp-generator 'SAFETY;SOLVED !'

# Blue stamp, more rotation, heavy wear
stamp-generator 'DO NOT;OPEN' --rotation -15 --color '#0044CC' --noise 0.7

# Clean green stamp, no wear
stamp-generator 'APPROVED' --color '#228B22' --noise 0 --output approved.png
```

## License

MIT
