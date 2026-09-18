<p align="center">
  <img src="https://static.ivao.aero/img/logos/logo.svg" />
</p>

<div align="center" width="100%">
<h1>IVAO Flatpak Repository</h1>
<p>The official Flatpak repository for IVAO desktop applications.</p>
<a href="https://ivaoaero.github.io/flatpak-repo/"><img alt="Repository" src="https://img.shields.io/badge/Flatpak-Repository-4a90e2"></a>
<a href="https://github.com/ivaoaero/flatpak-repo"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-ivaoaero%2Fflatpak--repo-181717?logo=github"></a>
</div>

## About

This repository distributes signed Flatpak applications developed and published by IVAO VzW.

The repository currently provides:

- **IVAO Altitude** - Pilot client for the IVAO flight simulation network.
- **IVAO Artifice** - IVAO flight simulation network connector.

Additional IVAO applications, including Aurora and mIVAO, may be added in the future.

## Requirements

1. A Linux distribution with [Flatpak](https://flatpak.org/) installed.
2. A compatible Flatpak runtime. Required runtimes are installed automatically by Flatpak when available.
3. An internet connection to access the repository and application runtimes.

## Usage

### Graphical software managers

The easiest way to install an IVAO application is through your desktop's software manager:

1. Make sure Flatpak support is enabled in your software manager and that the **Flathub** repository is available. Flathub provides the runtime required by the IVAO applications and is enabled by default on many distributions.
2. If Flathub is not available, open the [Flathub repository file](https://flathub.org/repo/flathub.flatpakrepo) in a web browser and confirm adding it to your software manager.
3. Open the [IVAO repository file](https://ivaoaero.github.io/flatpak-repo/ivao.flatpakrepo) in a web browser.
4. If the browser downloads the file instead of opening it, open the downloaded `.flatpakrepo` file with your software manager.
5. Confirm adding the IVAO repository when prompted.
6. Search for **IVAO Altitude** or **IVAO Artifice** and select **Install**.

On KDE Plasma, use **KDE Discover**. On GNOME, use **GNOME Software**. The exact button names can vary slightly depending on the desktop and distribution. If Flathub is not listed, enable it in the software manager's repository settings or install the Flatpak integration package provided by your distribution. If the IVAO repository file does not open automatically, make sure `.flatpakrepo` files are associated with the software manager.

After the repository has been added, application updates are handled by the normal update mechanism in Discover or GNOME Software.

Application-specific reference files are also available:

- [IVAO Altitude](https://ivaoaero.github.io/flatpak-repo/aero.ivao.Altitude.flatpakref)
- [IVAO Artifice](https://ivaoaero.github.io/flatpak-repo/aero.ivao.Artifice.flatpakref)

### Command line

You can also add the repository from a terminal:

If this is the first time you are using Flatpak, add Flathub first because it provides the runtime required by the IVAO applications:

```bash
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

Add the IVAO Flatpak repository:

```bash
flatpak remote-add --if-not-exists ivao https://ivaoaero.github.io/flatpak-repo/ivao.flatpakrepo
```

Install IVAO Altitude:

```bash
flatpak install ivao aero.ivao.Altitude
```

Install IVAO Artifice:

```bash
flatpak install ivao aero.ivao.Artifice
```

If you do not have administrator privileges, or prefer to install the applications only for your user account, add `--user` after `flatpak`:

```bash
flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak remote-add --user --if-not-exists ivao https://ivaoaero.github.io/flatpak-repo/ivao.flatpakrepo
flatpak install --user ivao aero.ivao.Altitude
flatpak install --user ivao aero.ivao.Artifice
```

Update installed IVAO applications:

```bash
flatpak update
```

Run the applications:

```bash
flatpak run aero.ivao.Altitude
flatpak run aero.ivao.Artifice
```

## License

The Altitude and Artifice license can be consulted at the following URL:
<https://wiki.ivao.aero/en/home/devops/manuals/end_user_licence_agreement-pilot>

---

Maintained by the IVAO Software Development Team from around the world.
