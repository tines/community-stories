# Billboard Number Ones
This Story sends you an email once a week with the number one song from the Billboard Hot-100 from five years ago along with a link which attempts to play it on Spotify in the browser.

It's a bit of a cheat tho. There are no good APIs for this information any more. So we scraped the data for 2016/2017/2018 and generated a CSV. You'll need to setup a MongoDB Atlas instance and import the CSV file into that. Then enable the new MongoDB Data API.

* Download the [JSON file](billboard-number-one-five-years-ago-today.json)
* Import it into your Tines account
* Download the [CSV file](billboard_number_ones_2016_to_2018.csv) and import it using:

```bash
mongoimport --uri mongodb+srv://USERNAME:PASWORD@MONGODB_SERVER_NAME/billboard --collection hot100 --type csv --file billboard_number_ones_2016_to_2018.csv --headerline
```

* Follow the remainder of the instructions in the Annotation inside the Story

![Number Ones](billboard_number_ones.png)
