# DefinitelyNotAVulnerableApp
This repository contains a vulnerable iOS app designed as a Capture The Flag (CTF) challenge for beginners. There are 5 easy flags to find, making it a great starting point for those new to iOS app security and reverse engineering.


## Walktrough (Contains Spoilers)
---

## Flag 1

<details>
<summary>Click to reveal spoiler</summary>

The flag is located in the Info.plist of the App. A straightforward `grep` command is sufficient to find it.

</details>

---

## Flag 2

<details>
<summary>Click to reveal spoiler</summary>

The flag is located in the PkgInfo as hexdump. Using `xxd` finds it.

</details>

---

## Flag 3

<details>
<summary>Click to reveal spoiler</summary>

The flag is hidden in an asset. Using a tool like [AssetCatalogTinkerer](https://github.com/insidegui/AssetCatalogTinkerer) to extract the assets reveals the flag.

</details>

---

## Flag 4

<details>
<summary>Click to reveal spoiler</summary>

The flag is hidden as a base64 string split in multiple parts in the binary. It can be found in the decompilation by searching for "==".

</details>

---

## Flag 5

<details>
<summary>Click to reveal spoiler</summary>

The flag is revealed by a method at runtime. Wee see in the decompilation that there is a "revealFlag" method. Attaching with lldb for example and calling the method will reveal the flag.

</details>
