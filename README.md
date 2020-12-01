# Computer-Programming-Project
from pyowm.owm import OWM
def temperatureMode(temperature_input):
    print('The average temperature is:',temperature_input)
    temperature = 0
    #sets the base of variable temperature to 0
    if int(temperature_input) in range(-100,45):
    #starts if statement using inputted temperature
    #if the inputted temperature is between -100-44...
        temperature = -1 
    #then temperature base is equal to -1
        print('Temperature is considered Low')
    #then print text "Low"
    elif int(temperature_input) in range(45,70):
    #starts else statement using inputted temperature
    #if the inputted temperature is between 45-70...
        temperature = 0
    #then temperature base remains as 0
        print('Temperature is considered Medium')
    #then print text "Medium"
    elif int(temperature_input) in range(70,1000):
    #starts else statement using inputted temperature
    #if the inputted temperature is between 70-1000...
        temperature = 1
    #then temperature base is equal to 1
        print('Temperature is considered High')
    #then print "High"
    return temperature
    #returns the temperature value so that code below can use it
    
def statusMode(status_input):
    status = 0
    #sets the base of variable status to 0
    if "rain" in status_input or "snow" in status_input or "storm" in status_input or "showers" in status_input:
    #starts if statement using inputted status
    #if the status input has any of the keywords...
        status = -1 
    #then the status base is equal to -1
        print('Weather status is considered Low')
    #then print "Low"
    elif "cloud" in status_input or "scattered" in status_input:
    #starts else statement using inputted status
    #if the status input has any of the keywords...
        status = 0
    #then status base remains 0
        print('Weather status is considered Medium')
    #then print "Medium"
    elif "sun" in status_input or "clear" in status_input:
    #starts elif statement using inputted status
    #if the status input has any of the keywords...
        status = 1
    #then status base is equal to 1
        print('Weather status is considered High')
    #then print "High"
    return status
    #returns the status value so that the code below can use it

def windMode(wind_input):
    wind = 0
    #sets the base of wind speed to 0
    if int(wind_input) in range(0,5):
    #starts if statement using inputted wind speed
    #if the wind speed is between 0-4.99...
        wind = -1 
    #then wind speed base is equal to -1
        print('Wind speed is considered Low')
    #then print "Low"
    elif int(wind_input) in range(5,10):
    #starts elif statement using inputted wind speed
    #if the wind speed is between 5-9.99...
        wind = 0
    #then the base of wind speed remains 0
        print('Wind speed is considered Medium')
    #then prints "Medium"
    elif int(wind_input) in range(10,100):
    #starts elif statement using inputted wind speed
    #if the wind speed is between 10-99.99...
        wind = 1
    #then the base of wind speed is equal to 1
        print('Wind speed is considered High')    
    #then prints "High"
    return wind
    #returns the wind value so that the code below can use it

def suggestions(temperature, status, wind):
    clothing = [0,0,0,0,0,0,0]
    #[jacket, long pants, short pants, long sleeve shirt, short sleeve shirt, hoodie, umbrella]
    #item of clothing corresponds to the order in which the clothing = [0..0] is listed as
    if temperature == -1 and status == -1 and wind == -1:
    #utilizes the defined temperature,wind, and status values with the information received from desired location to suggest what item of clothing to bring on the trip.
    #the item suggestions were based off of what the group would wear on such weather
        print('It is recommended you bring a jacket, long pants, long sleeve shirt, and an umbrella.')
        #prints out text suggesting what to wear
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
        clothing[6] += 1
        #the lines of code above help summarize the total number of each items to bring at the end of the trip
    elif temperature == -1 and status == -1 and wind == 0:
        print('It is recommended you bring a jacket, long pants, long sleeve shirt, and an umbrella.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
        clothing[6] += 1
    elif temperature == -1 and status == -1 and wind == 1:
        print('It is recommended you bring a jacket, long pants, long sleeve shirt, and an umbrella.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
        clothing[6] += 1
    elif temperature == -1 and status == 0 and wind == -1:
        print('It is recommended you bring a jacket, long pants, and a long sleeve shirt.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
    elif temperature == -1 and status == 0 and wind == 0:
        print('It is recommended you bring a jacket, long pants, and a long sleeve shirt.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
    elif temperature == -1 and status == 0 and wind == 1:
        print('It is recommended you bring a jacket, long pants, and a long sleeve shirt.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
    elif temperature == -1 and status == 1 and wind == -1:
        print('It is recommended you bring a jacket, long pants, and a long sleeve shirt.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
    elif temperature == -1 and status == 1 and wind == 0:
        print('It is recommended you bring a jacket, long pants, and a long sleeve shirt.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
    elif temperature == -1 and status == 1 and wind == 1:
        print('It is recommended you bring a jacket, long pants, and a long sleeve shirt.') 
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
        
    elif temperature == 0 and status == -1 and wind == -1:
        print('It is recommended you bring a hoodie, long pants, short sleeve shirt, and an umbrella.')
        clothing[5] += 1
        clothing[1] += 1
        clothing[4] += 1
        clothing[6] += 1
    elif temperature == 0 and status == -1 and wind == 0:
        print('It is recommended you bring a jacket, long pants, short sleeve shirt, and an umbrella.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[4] += 1
        clothing[6] += 1
    elif temperature == 0 and status == -1 and wind == 1:
        print('It is recommended you bring a jacket, long pants, long sleeve shirt, and an umbrella.')
        clothing[0] += 1
        clothing[1] += 1
        clothing[3] += 1
        clothing[6] += 1
    elif temperature == 0 and status == 0 and wind == -1:
        print('It is recommended you bring short pants, and a short sleeve shirt.')
        clothing[2] += 1
        clothing[4] += 1
    elif temperature == 0 and status == 0 and wind == 0:
        print('It is recommended you bring short pants, and a long sleeve shirt.')
        clothing[2] += 1
        clothing[3] += 1
    elif temperature == 0 and status == 0 and wind == 1:
        print('It is recommended you bring a hoodie, long pants, and a long sleeve shirt.')
        clothing[5] += 1
        clothing[1] += 1
        clothing[3] += 1
    elif temperature == 0 and status == 1 and wind == -1:
        print('It is recommended you bring short pants and a short sleeve shirt.')
        clothing[2] += 1
        clothing[4] += 1
    elif temperature == 0 and status == 1 and wind == 0:
        print('It is recommended you bring short pants and a short sleeve shirt.')
        clothing[2] += 1
        clothing[4] += 1
    elif temperature == 0 and status == 1 and wind == 1:
        print('It is recommended you bring long pants and a long sleeve shirt.') 
        clothing[1] += 1
        clothing[3] += 1

    elif temperature == 1 and status == -1 and wind == -1:
        print('It is recommended you bring long pants, short sleeve shirt, and an umbrella.')
        clothing[1] += 1
        clothing[4] += 1
        clothing[6] += 1
    elif temperature == 1 and status == -1 and wind == 0:
        print('It is recommended you bring a hoodie, long pants, short sleeve shirt, and an umbrella.')
        clothing[5] += 1
        clothing[1] += 1
        clothing[4] += 1
        clothing[6] += 1
    elif temperature == 1 and status == -1 and wind == 1:
        print('It is recommended you bring a hoodie, long pants, short sleeve shirt, and an umbrella.')
        clothing[5] += 1
        clothing[1] += 1
        clothing[4] += 1
        clothing[6] += 1
    elif temperature == 1 and status == 0 and wind == -1:
        print('It is recommended you bring short pants and a short sleeve shirt.')
        clothing[2] += 1
        clothing[4] += 1
    elif temperature == 1 and status == 0 and wind == 0:
        print('It is recommended you bring short pants and a short sleeve shirt.')
        clothing[2] += 1
        clothing[4] += 1
    elif temperature == 1 and status == 0 and wind == 1:
        print('It is recommended you bring short pants and a long sleeve shirt.')
        clothing[2] += 1
        clothing[3] += 1
    elif temperature == 1 and status == 1 and wind == -1:
        print('It is recommended you bring short pants and a short sleeve shirt.')
        clothing[2] += 1
        clothing[4] += 1
    elif temperature == 1 and status == 1 and wind == 0:
        print('It is recommended you bring short pants and a short sleeve shirt.')
        clothing[2] += 1
        clothing[4] += 1
    elif temperature == 1 and status == 1 and wind == 1:
        print('It is recommended you bring long pants and a short sleeve shirt.') 
        clothing[1] += 1
        clothing[4] += 1

    return clothing
    #returns the variable clothing so that the code below can use it
#imports OWM weather API 
owm = OWM('e8e9f0f003e2960fd0a1451e969b99ea')
#OMW API  key code
mgr = owm.weather_manager()
#calls OMW manager
reg = owm.city_id_registry()
#list of cities
x = input('Please enter your desired city location: ')
y = input('Please enter your desired state/territory/country in two-letter abbreviations: ')
list_of_locations = reg.locations_for(x, y)
#location chosen for vacation
location = list_of_locations[0]
lat = location.lat  
#latitude of location is represented as lat
lon = location.lon  
#longitutde of location is represented as long 
print(lat, lon)
#prints the latitude and longitude of the inputted location 
one_call = mgr.one_call(lat, lon)
#utilizes API to find the latitutde and longitude of desired location
#need the latitude and longitude of locaiton to find information
days = 0
#day count starting at 0
clothing = [0,0,0,0,0,0,0]
for weather in one_call.forecast_daily:
#utilizes one_call function in OWM API to print desired 
    print('----------------')
    #prints ----- in between each day count to separate days and make everything organized
    print("Day " + str(days))
    #prints string of days starting at 0
    print('Lowest Temperature(Fahrenheit): ' + str(weather.temperature('fahrenheit')['min']) + '\nHighest Temperature(Fahrenheit): ' + str(weather.temperature('fahrenheit')['max']))
    #prints string of lowest and highest temperature according to the longitude and latitude geographical locations that the user inputted 
    print('Weather: ' + str(weather.detailed_status))
    #prints string of detailed weather status according to the longitude and latitude geographical locations that the user inputted 
    print('Wind Speed(m/s): ' + str(weather.wind()['speed']))
    #prints string of weather according to the longitute and latitude geographical locations that the user inputted 
    print('Humidity(%): ' + str(weather.humidity))
    #prints string of humidity according to the longitude and latitude geographical locations that the user inputted
    days += 1
    #the count of days increase at increments of 1
    temperature = temperatureMode(((weather.temperature('fahrenheit')['min']) + (weather.temperature('fahrenheit')['max']))//2)
    #uses the code from line 2-27 to print whether or not the temperature is low, medium, or high
    status = statusMode(weather.detailed_status)
    #uses the code from line 57-81 to print whether or not the status is low, medium, or high
    wind = windMode(weather.wind()['speed'])
    #uses the code from line 30-54 to print whether or not the wind speed is low, medium, or high
    temp = suggestions(temperature, status, wind)
    for i in range(len(clothing)):
        clothing[i] += temp[i]
        #counts the total number of items of clothing 
print('----------------')
#prints a divider between day 7 and the texts below
print("You want to bring " + str(clothing[0]) + " jacket(s)." )
#summarizes the total number of jackets to bring for the week
print("You want to bring " + str(clothing[1]) + " long pants.")
#summarizes the total number of long pants to bring for the week
print("You want to bring " + str(clothing[2]) + " short pants.")
#summarizes the total number of short pants to bring for the week
print("You want to bring " + str(clothing[3]) + " long sleeve shirt(s).")
#summarizes the total number of long sleeve shirts to bring for the week
print("You want to bring " + str(clothing[4]) + " short sleeve shirt(s).")
#summarizes the total number of short sleeve shirts to bring for the week
print("You want to bring " + str(clothing[5]) + " hoodie(s).")
#summarizes the total number of hoodies to bring for the week
print("You want to bring " + str(clothing[6]) + " umbrella(s).")
#summarizes the total number of umbrellas to bring for the week
