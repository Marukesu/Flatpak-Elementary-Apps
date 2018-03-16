# Flatpaked elementary applications

**This is a unofficial repo for flatpak apps of elementary os.** see your distro package manager for the official packages or build it from the [elementary's GitHub repo](https://github.com/elementary)

## Status
All apps begin with "(Git)" in their names because its form git master and for not confusing with the officials apps

| Application | Status |
| --- | --- |
| io.elementary.calculator | OK |
| io.elementary.code | OK |
| io.elementary.screenshot-tool | OK |

**OBS:** more apps are coming when the manifests becomes buildable

## Build the manifest and install

Flatpak-builder is needed since its only manifest, so, for example, you will install code runing...

`flatpak-builder .build io.elementary.code.json --install`

or if your wanna make a local repo, in ~/.elementaryFlat folder, and install for it. run

```
flatpak-builder --repo=/home/user/.elementaryFlat .build io.elementary.code.json
flatpak remote-add ~/.elementaryFlat elementaryApps
flatpak install elementaryApps io.elementary.code
```

remember of rebuild the manifest when it's have a update in git. it's can be easlly with the `--require-changes` option of flatpak-builder
