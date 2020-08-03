# Employee-Details
import json
import datetime
from datetime import date
import calendar
f = open('Test.json', )
Test = json.load(f)
for i in Test['members']:
    print("id:", i['id'])
    print("real_name", i['real_name'])
    print("tz", i['tz'])
    print("activity_periods", i['activity_periods'])
    date=str(input('Enter the date'))
    day_name= ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday','Sunday']
    day = datetime.datetime.strptime(date, '%d %m %Y').weekday()
    print(day_name[day])
f.close()
