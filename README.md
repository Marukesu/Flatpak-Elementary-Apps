# elementary sandbox-ed applications

**This is a unofficial repository for flatpak manifests of elementary OS apps.** see your distro package manager for the official packages or build them from the [elementary's GitHub repo](https://github.com/elementary)

## Status

| Application | status |
| --- | --- |

| io.elementary.calculator | OK |
| io.elementary.code | OK |
| io.elementary.music | OK |
| io.elementary.screenshot | * |
| io.elementary.videos | * |

## Build the manifest and install

You'll need to compile the [elementary's flatpak platform](https://github.com/elementary/flatpak-platform) to use theses manifests.
Flatpak-builder is needed for build the manifests, so, for example, you will install code running: 

`flatpak-builder --user .build io.elementary.code.yml --force-clean --install`

or,your wanna make a local repo and install form it. run:

```
flatpak-builder --user .build io.elementary.code.yml --repo=/home/user/.elementaryFlat
flatpak remote-add --user --no-gpg-verify ~/.elementaryFlat elementaryApps
flatpak install elementaryApps io.elementary.code
```
so now you'll have a unique repo for all the apps.
