# AI Linux Packages

This repository contains `.deb` and `.rpm` repositories for various AI-related tools and applications on Linux. Packages are automatically built and published to Debian and RPM repositories hosted via GitHub Pages.

## Disclaimer

**The Gemini CLI package is currently not working.**

## Installation

### Debian/Ubuntu

To use this repository on your Debian-based system (Ubuntu, Linux Mint, Debian, etc.), follow the steps below.

#### 1. Add the Repository

```bash
echo "deb [trusted=yes] https://ai-linux.koca.dev/deb stable main" | sudo tee /etc/apt/sources.list.d/ai-linux.list
```

#### 2. Update and Install

After adding the repository, update your package index and install the desired packages:

```bash
sudo apt update
sudo apt install <package-name>
```

### Fedora/CentOS/RHEL

To use this repository on your RPM-based system (Fedora, CentOS, RHEL, etc.), follow the steps below.

#### 1. Add the Repository

Create a file named `/etc/yum.repos.d/ai-linux.repo` with the following content:

```
[ai-linux]
name=ai-linux repository
baseurl=https://ai-linux.koca.dev/rpm
enabled=1
gpgcheck=0
```

#### 2. Install

After adding the repository, you can install the desired packages:

```bash
sudo dnf install <package-name>
```

## Contributing

To add a new package or update an existing one:

1.  Create or modify [a `.koca` file](https://github.com/koca-build/koca) in the `koca/` directory.
2.  Push your changes to the `main` branch.
3.  The GitHub Actions workflow will automatically build the package, create a GitHub Release, and update the Debian and RPM repositories.

## License

The build scripts in this repository are released under the [MIT License](LICENSE).
