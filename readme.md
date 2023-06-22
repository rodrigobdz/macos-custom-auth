# macos-custom-auth

> Enables TouchID and YubiKey as authentication methods by modifying your Pluggable Authentication Modules (PAM).

After each macOS update, the PAM config is reset to the default. This script will replace the default PAM config with one that enables TouchID and YubiKey as authentication methods.

## Disclaimer

**WARNING:** This is a proof of concept. Use at your own risk!

**IMPORTANT:** Back up your system before using this script.

**DANGER:** It is considered a security risk to modify your PAM config and it could lock you out of your system forever.

**Use this script only if you understand the risks.**

## Requirements

- [Install YubiKey pam module](https://formulae.brew.sh/formula/pam_yubico)

## Usage

- Enable TouchID and YubiKey as authentication methods

    Compares changes, backs up existing modules in `/etc/pam.d/` and replaces them with the contents of `./etc/pam.d/`.

    ```sh
    sudo ./script/replace-pam-d-modules
    ```

## Further Reading

- [YubiKey Challenge-Response](https://developers.yubico.com/yubico-pam/Authentication_Using_Challenge-Response.html)
