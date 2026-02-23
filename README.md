# AI Linux Packages

This repository contains `.deb` repositories for various AI-related tools and applications on Linux. Packages are automatically built and published to a Debian repository hosted via GitHub Pages.

## Usage

To use this repository on your Debian-based system (Ubuntu, Linux Mint, Debian, etc.), follow the steps below.

### 1. Add the Repository

Since this repository is currently unsigned, you must explicitly trust it when adding it to your sources:

```bash
echo "deb [trusted=yes] https://hwittenborn.github.io/ai-linux/ stable main" | sudo tee /etc/apt/sources.list.d/ai-linux.list
```

### 2. Update and Install

After adding the repository, update your package index and install the desired packages:

```bash
sudo apt update
sudo apt install <package-name>
```

## Contributing

To add a new package or update an existing one:

1.  Create or modify [a `.koca` file](https://github.com/koca-build/koca) in the `koca/` directory.
2.  Push your changes to the `main` branch.
3.  The GitHub Actions workflow will automatically build the package, create a GitHub Release, and update the Debian repository.

## License

The build scripts in this repository are released under the [MIT License](LICENSE).
