# MyObservatory

This is a test script to presnet automation test for Android application MyObservatory

# Request of test case 
1. Launcher app
2. Open Side Menu
3. Select item: 9-Day Weather Forecast
4. Verify Forecast of the next 9 days are displayed

# How scritp judge its FAIL
1. fail to select "HK 9-day weather forecast" button in side menu
2. fail to open HK 9-day weather forecast page
3. fail to collect 9-day forecast data on page ( e.g. if we only found 8 days data, test will set to fail)

# Environment ( this is the environment i run this script so it nice you can have similar things before you run it)
1. Macbook pro running on IOS 10.12.3
2. Appium v1.6.5
3. Python 3.6
4. Python package, Appium-Python-Client(0.24), pytest(3.2.0), selenium(3.4.3)
5. Android application MyObservatory, please download it from Google play store

# Must know
Please modify desired caps to fit your test device. 

my condig is:
platformVersion': '7.1.2', 'deviceName': 'Nexus 5X'

but you should modify above data in test script to fit your environment

# Usage
1. clone to local machine
2. start appium service
3. run  "python HKO.py"
4. check console log also status on device
5. you also can check screenshots of HK 9days forecast page to manually verification

# Known issue
Sometimes it fails when finding item "HK 9 Day forecast" in side menu. the script seems not did the "swipe" action on device
I haven't digged into why this happend.
The workaround is to kill and restart your appium service. Then run scritp agian.


