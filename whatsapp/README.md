# Install WhatsApp w/o Microsoft Store

## **Downloading**

Get the direct URL of the app from the Microsoft Store website.

As of writing this, it's [https://apps.microsoft.com/store/detail/whatsapp/9NKSQGP7F2NH?hl=en-us&gl=us](<https://apps.microsoft.com/store/detail/whatsapp/9NKSQGP7F2NH?hl=en-us&gl=us>) (Unsure if it will be changed in the future)

Paste that URL into [https://store.rg-adguard.net/](<https://store.rg-adguard.net/>)

Download the latest (by date) WhatsAppDesktop file that ends with .msixbundle (The size should be around 100MB)

## **Installation**

Run Windows PowerShell (admin).

Paste the following command line changing whatever is necessary for your download location file path.

```
Add-AppxPackage -Path 'C:\Users\*USERNAME*\Downloads\*FILENAME*.Msixbundle'
```

If you get some error, it's probably because you lack some [Windows Dependencies.](<https://github.com/erphise/WindowsDependencies> "Windows Dependencies")

Download the ones needed and run this command for each one of them:

```
Add-AppxPackage -Path 'C:\Users\*USERNAME*\Downloads\*DEPENDENCIE_NAME*.Appx'
```

Once all the dependencies are installed, you can try again. Now it should work.

Let it do it’s thing after that, and the application will be installed successfully.



