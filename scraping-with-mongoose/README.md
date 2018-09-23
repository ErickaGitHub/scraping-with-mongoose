# scraping-with-mongoose





Run npm init. 

When that's finished, install and save these npm packages:
express
express-handlebars
mongoose
body-parser
cheerio
request



In order to deploy your project to Heroku, you must set up an mLab provision. mLab is remote MongoDB database that Heroku supports natively. Follow these steps to get it running:
Create a Heroku app in your project directory.
Run this command in your Terminal/Bash window:


* `heroku addons:create mongolab`

* This command will add the free mLab provision to your project.



// If deployed, use the deployed database. Otherwise use the local mongoHeadlines database
var MONGODB_URI = process.env.MONGODB_URI || "mongodb://localhost/mongoHeadlines";

// Set mongoose to leverage built in JavaScript ES6 Promises
// Connect to the Mongo DB
mongoose.Promise = Promise;
mongoose.connect(MONGODB_URI);






 * Headline - the title of the article

 * Summary - a short summary of the article

 * URL - the url to the original article

 * Feel free to add more content to your database (photos, bylines, and so on).




//////TIPS/////
Whenever you scrape a site for stories, make sure an article isn't already represented in your database before saving it; we don't want duplicates.

Don't just clear out your database and populate it with scraped articles whenever a user accesses your site.


If your app deletes stories every time someone visits, your users won't be able to see any comments except the ones that they post.





