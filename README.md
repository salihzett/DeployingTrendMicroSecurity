# Deploying TrendMicro Worry-Free Security Services agent
###### a little tutorial to create a trendmicro-installer for macOS deployment - with composer (but u can use any pkg-create-tool)


### Step 1: Downloading Installer Package
1. Go to the [Trend Micro Security Website](https://wfbs-svc-emea.trendmicro.com/) 
2. Click *Device* and choose your Device Group
3. Click *Add Devices* and choose under *Install to this Device* -> Install
![1](images/Screenshot1.png)
4. Next step click *Download* and download the package on your mac.
![2](images/Screenshot2.png)

### Step 2: Creating deploy script "Identifier.plist"
1. Go to the [Trend Micro Security Website](https://wfbs-svc-emea.trendmicro.com/), click on *Device* and choose your Device Group
2. Click *Add Devices* again and choose under *Download the Installer Package (Advanced)* -> *For Service Providers*
3. Get your *Identifier* by clicking on the button *Copy Identifier*
![3](images/Screenshot3.png)
4. Put the *Identifier* in a plist file. Replace "PutYourIdentifier" parameter with your Identifier. (Use my default plist file in the repo)
```plist
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>Identifier</key>
	<string>#PutYourIdentifier</string>
</dict>
</plist>
```

### Step 3: Distributable package with composer
