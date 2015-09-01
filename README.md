# google-docs-heatmap

Generate a heat-map of writing based on data from the [Google Docs Writing Tracker](https://github.com/jamietr1/google-docs-writing-tracker). When implemented on a website, the results will look something like this:

![Heatmap](https://github.com/jamietr1/google-docs-heatmap/blob/master/images/heatmap.png)

## Prerequisites

1. You must already be using the [Google Docs Writing Tracker](https://github.com/jamietr1/google-docs-writing-tracker). This is the data source for the heatmap.
2. You must have your own website, or a place where you can host the code that generates the heatmap.
3. You must [install](http://cal-heatmap.com/#installation) the Cal-heatmap javascript module. The code is [available on Github](https://github.com/wa0x6e/cal-heatmap).

## Installation

In order to be able to produce a heatmap of writing data, you need to publish the Google Docs Writing Tracker spreadsheet so that a script can access the data. You only need to publish the Writing tab.

1. Publish the Writing sheet of your Google Docs Writing Tracker spreadsheet as a CSV file.
  * Open your Google Docs Writing Tracker spreadsheet
  * From the File menu, click Publish to the Web...
  * Under the Link options, select just the Writing sheet.
  * Select Comma-separated values (.csv)
  * Copy the link provided for the published sheet.

  ![Publish to the web](https://github.com/jamietr1/google-docs-heatmap/blob/master/images/Publish.png)

2. Copy the heatmap.php file to your website.
3. Paste the URL from step 1 between the quotes in line 4:

  `$google_docs_writing_sheet = "URL from step 1 goes here"`

4. Copy heatmap.html to your website
5. Update any references in the HTML file to where you installed the cal-heatmap library.
6. Line 15 should point to the location of your heatmap.php file:

  `data: "http://yourwebsite.com/scripts/heatmap.php"`

With that done, you should be able to go to the heatmap.html file and see the heatmap for your writing data.

For an example of this in action, check out [my heatmap](http://open.jamierubin.net/v8/heatmap.html).
