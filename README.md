# RuneHistory Highscore Microservice

This microservice manages highscores for accounts.
* Aggregates new highscores on submission from the Collecter service.
* Returns highscore stats for the requested account, skill(s), and period.
* Returns a sorted list of accounts who have achieved the highest gain in XP for the given skill(s) and period.

Accepted time periods should be:
* `hour`: The past hours data. Grouped to every 5 mins of data. Max 12 records returned.
* `24_hour`: The past 24 hours of data. Grouped to every 10 mins of data. Max 144 records.
* `7_day`: The past 7 days (168 hours) of data. Grouped up to every hour of data. Max 168 records.
* `30_day`: The past 30 days (720 hours) of data. Grouped to 4 hours of data. Max 180 records.
