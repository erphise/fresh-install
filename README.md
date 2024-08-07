# Windows 11

## Download / How to use it?

### Method 1 - PowerShell (Recommended)

- Right-click on the Windows start menu and select PowerShell or Terminal (Not CMD).

- Copy and paste the code below and press enter

```text
irm https://get.activated.win | iex
```

or

```text
irm https://massgrave.dev/get | iex
```

- You will see the activation options. Follow the on-screen instructions.

- That's all.

---

- On older Windows builds you may need to run the below command before,
    `[Net.ServicePointManager]::SecurityProtocol=[Net.SecurityProtocolType]::Tls12`

- The Powershell method does not work on Windows 7. Use the Method 2 - Traditional instead.

- The URL [get.activated.win](<http://get.activated.win>) may be blocked by some DNS services because it is a new domain.

### Method 2 - Traditional

- Download the file under the code button from [GitHub](<https://github.com/massgravel/Microsoft-Activation-Scripts>) or [Bitbucket](<https://bitbucket.org/WindowsAddict/microsoft-activation-scripts>)

- Right-click on the downloaded zip file and extract

- In the extracted folder, find the folder named `All-In-One-Version`

- Run the file named `MAS_AIO-CRC32_XXXXXXXX.cmd`

- You will see the activation options, follow the on-screen instructions.

- That's all.

To run the scripts in unattended mode, check [here.](<https://massgrave.dev/command_line_switches>)

---

## Activation Summary

| Activation Type                      | Supported Product                    | Activation Period                    |
| ------------------------------------ | ------------------------------------ | ------------------------------------ |
| HWID                                 | Windows 10-11                        | Permanent                            |
| Ohook                                | Office                               | Permanent                            |
| KMS38                                | Windows 10-11-Server                 | Till the Year 2038                   |
| Online KMS                           | Windows / Office                     | 180 Days. Lifetime With Renewal Task |

To activate unsupported products such as **Office on Mac**, check [here](<https://massgrave.dev/unsupported_products_activation>).

---

# Install chocolatey

## Requirements

- [Supported Windows client and server Operating Systems](<https://docs.chocolatey.org/en-us/chocolatey-components-dependencies-and-support-lifecycle#supported-windows-versions>) (can run on older Operating Systems)

- PowerShell v2+ (minimum is v3 for install from this website due to [TLS 1.2 requirement](<https://chocolatey.org/blog/remove-support-for-old-tls-versions>))

- .NET Framework 4.8 (the installation will attempt to install .NET 4.8 if you do not have it installed)

## Installation

1. First, ensure that you are using an [***administrative shell***](<https://www.howtogeek.com/194041/how-to-open-the-command-prompt-as-administrator-in-windows-10/>) \- you can also install as a non-admin, check out [Non-Administrative Installation](<https://docs.chocolatey.org/en-us/choco/setup#non-administrative-install>).

2. Install with powershell.exe

<div data-block-id="HSlFXfKj" data-callout-type="info" class="callout"><h4 data-block-id="LMpXbI_q">INFO</h4><p data-block-id="JabVuoge" data-spacing="double">Please inspect <a target="_blank" rel="noopener noreferrer nofollow" href="https://community.chocolatey.org/install.ps1">https://community.chocolatey.org/install.ps1</a> prior to running any of these scripts to ensure safety. We already know it's safe, but you should verify the security and contents of <strong><em>any</em></strong> script from the internet you are not familiar with. All of these scripts download a remote PowerShell script and execute it on your machine. We take security very seriously. <a target="_blank" rel="noopener noreferrer nofollow" href="https://docs.chocolatey.org/en-us/information/security">Learn more about our security protocols</a>.</p></div>

With PowerShell, you must ensure [Get-ExecutionPolicy](<https://go.microsoft.com/fwlink/?LinkID=135170>) is not Restricted. We suggest using `Bypass` to bypass the policy to get things installed or `AllSigned` for quite a bit more security.

- Run `Get-ExecutionPolicy`. If it returns `Restricted`, then run `Set-ExecutionPolicy AllSigned` or `Set-ExecutionPolicy Bypass -Scope Process`.

Now run the following command:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

3. Paste the copied text into your shell and press Enter.

4. Wait a few seconds for the command to complete.

5. If you don't see any errors, you are ready to use Chocolatey! Type `choco` or `choco -?` now, or see [Getting Started](<https://docs.chocolatey.org/en-us/getting-started>) for usage instructions.