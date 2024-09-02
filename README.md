##### Ever wanted to make a plant monitoring system for your garden but put off by the amount of coding required. Well, I have some good news.

# What is Pi Grow?

Pi Grow is a web app designed to help users create their custom plant monitoring system and a web page dashboard to view all the data, all with a few clicks.

Website hosted at [Pi-grow](https://raspberry-pi-plant-monitoring.web.app/).

## How to use?

Currently supports the following sensors: 

*  BMP280 --Temperature and pressure 
*  SEN0193--soil moisture 
*  BH1750--light intensity
*  Pi camera module v2


1. Attach your sensors to the raspberry pi. See github repo for guide.

2. Git clone rasp-pi-sensor-data.. repo onto you raspberry pi. I recommend creating and activating a virtual  environment at this stage before install dependencies for consistant results.

```bash
git clone https://github.com/Vinod2311/Rasp-pi-Sensor-Data-Collection-and-Cloud-Upload.git
```

3. Install python and node dependencies.

```bash
npm install
pip3 install requirements.txt
```

4. Sign up at [Link to website](https://raspberry-pi-plant-monitoring.web.app/). Choose your system settings( sensors used, measurement timing etc. ).

5. Update the file user.json with your own details.

6. Run sensor script

```bash
python3 main.py
```
If you plan to keep the script running even after you disconnect from your pi, I recommend using the `screen` package.


## Using the web app

A database is automatically created for you to hold your data. You can create a dashboard view on the dashboard page.

Add different widgets to your dashboard. Resize, move and customise your page.

![Dashboard view](docs/final-product.JPG?raw=true "Title")


## Attaching sensors to a raspberry pi

#### BMP280 - Temp and Pressure

Setup for using this sensor. You may need to solder the sensor onto a header.
![temp sensor](docs/bmp280.JPG?raw=true "Title")

The following is a good guide. [Link to website](https://docs.sunfounder.com/projects/umsk/en/latest/05_raspberry_pi/pi_lesson20_bmp280.html)

#### SEN0193--soil moisture 

Setup for using this sensor. You will need an ADC to allow the pi to read the sensor. I used MCP3008.
![soil moisture sensor](docs/moisture-sensor-setup.JPG?raw=true "Title")


#### BH1750--light intensity

You may need to solder the sensor onto a header.

![soil moisture sensor](docs/bh1750.png?raw=true "Title")
The following is a good guide. [Link to website](https://learn.adafruit.com/adafruit-bh1750-ambient-light-sensor/python-circuitpython)



## License

[MIT](https://choosealicense.com/licenses/mit/)
