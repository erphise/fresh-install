# First Windows 11 Install

<div data-block-id="8DbjhJfR" data-callout-type="info" class="callout"><h4 data-block-id="eQfuLsVF">DO THIS FIRST</h4><p data-block-id="8nvdKmCQ" data-spacing="double">Download <a target="_blank" rel="noopener noreferrer nofollow" title="Win11 IoT Enterprise LTSC 2024" href="https://massgrave.dev/windows_ltsc_links#win11-iot-enterprise-ltsc-2024">Win11 IoT Enterprise LTSC 2024</a> ISO from MAS.</p></div>

# Download / How to use it?

## Method 1 - PowerShell (Recommended)

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

## Method 2 - Traditional

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



