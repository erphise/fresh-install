# Custom Installation Guide

First, you'll need to clear previous installations of Office. You can skip this if Office has never been installed on the machine before:

- Uninstall Office with the App and Features option in Windows settings.

- Run `OfficeScrubber.cmd` file from [Office Scrubber](<https://github.com/abbodi1406/WHD/raw/master/scripts/OfficeScrubber_12r.zip>) by abbodi1406 and select `[R] Remove all Licenses` option.

Once you're done:

- Download [Office Deployment Tool](<https://officecdn.microsoft.com/pr/wsus/setup.exe>) (ODT)

- Copy the downloaded `setup.exe` file to the root of the C drive, i.e. `C:\setup.exe`

- Go to [config.office.com](<http://config.office.com>)

- If you want Retail Office then select `Microsoft 365 Apps for enterprise` in the office suites section.

- If you want Volume Office then select `Office LTSC Professional Plus 2021 - Volume License` in the office suites section. (Don't select the SPLA version)

- You can add Visio and Project apps if you need them. Don't select language that is [not available for Project/Visio](<https://gravesoft.dev/office_c2r_links>) if you are installing those apps.

- Customize other things and leave settings as default if you don't understand something.

- Once you go through all the options, click on the export button, select "Keep Current Settings" option and it will download a file named `Configuration.xml`

- Copy the downloaded `Configuration.xml` file to the root of the C drive, i.e. `C:\Configuration.xml`

- Open the command prompt as admin and run the below commands

    ```text
    cd /d C:\
    setup.exe /configure Configuration.xml
    ```

It will now download and install Office. You can activate it with your preferred method.



