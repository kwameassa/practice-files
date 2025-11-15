# practice-files

This repository contains practice files students will use when following the Ubuntu OS installation lessons.

This README explains two easy ways to get the files using the Ubuntu terminal:

- Option A — clone the repository using Git (recommended if you plan to make changes or submit work)
- Option B — download the ZIP archive and extract it (quick download, no Git needed)

## Prerequisites

Open the Terminal (Ctrl+Alt+T) and ensure you have the required tools. Run:

```bash
sudo apt update
sudo apt install -y git unzip wget
```

Notes:
- `git` is needed for cloning with Git.
- `unzip` is needed to extract a downloaded ZIP file.
- `wget` is used to download the ZIP archive from GitHub.

## Option A — Clone with Git (recommended)

1. In your terminal choose (or create) the folder where you want the files, e.g. your home directory or `~/projects`:

```bash
cd ~
mkdir -p projects
cd projects
```

2. Clone the repository:

```bash
git clone https://github.com/kwameassa/practice-files.git
```

3. Move into the project folder and list the files:

```bash
cd practice-files
ls -la
```

You now have the repository locally and can open files in an editor or follow your lesson instructions.

## Option B — Download ZIP and extract

1. From the terminal, download the repository's ZIP archive from GitHub:

```bash
cd ~
mkdir -p downloads
cd downloads
wget https://github.com/kwameassa/practice-files/archive/refs/heads/main.zip -O practice-files.zip
```

2. Unzip the archive and inspect the contents:

```bash
unzip practice-files.zip
cd practice-files-main
ls -la
```

3. (Optional) Move or rename the extracted folder for convenience:

```bash
mv ~/downloads/practice-files-main ~/projects/practice-files
cd ~/projects/practice-files
```

## Verifying the files

Make sure you see the expected files. From inside the repository folder run:

```bash
pwd
ls -la
```

The `pwd` output should end with `practice-files` (or `practice-files-main` if you used the ZIP option). If you cloned with Git you can also check the current commit and branch:

```bash
git status --short
git rev-parse --abbrev-ref HEAD
```

## Troubleshooting

- Permission denied when installing packages: ensure you run `sudo` and that your user has sudo rights.
- `git: command not found` or `unzip: command not found`: install the correct package (see Prerequisites section).
- Network/download issues: check your internet connection and try again; you can also try cloning/downloading from a different network.

## Additional notes

- If you plan to submit changes or push to your own fork, create a GitHub account and fork the repository first. Then clone your fork instead of this repository.
- For classroom use we recommend Option A (git clone) so students can track changes and submit work using Git.

If you need anything changed in these instructions (more screenshots, Windows or macOS steps, or specific examples), open an issue or ask your instructor.

