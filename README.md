# Python-project for Wikipedia Watching.
The code available here are divided into two tasks!

Things to know before using the code:
1. This code was done in jupyter Notebook, but the code can still work as a regular python file to.
2. The library SSEClient might not be installed by default, so please install it.
3. There is an interrupt which is present inside the code, which checks for any interrupts and then terminates the program. In jupyter notebook click on "interrupt kernal button " to stop the program. For people who use the code outside of jupyter notebook, give any keyboard interrupt.If it doesn't work force stop the program. 
4. To strart the code just run the python code and it'll start, the output will be displayed in the console/terminal.
5. Currently the output will be displayed every 10 secs for Task1 and every 5 sec for task 2. If you want to change the timing for your reference change that within the code in the fetch_data function.

Below is the Problem Statement of the code.

Task 1
Keep track of the data coming on the API and every 1 minute, generate the two reports. The reports should be based on the data received in the last 1 minute. The reports should be printed on the terminal/console.

Task 2
While reports based on 1 minute data are useful, we would like to keep track of the changes over a larger window of time. We will now start generating reports based on 5 minutes worth of data instead of 1 minute.

There are 2 reports to be generated:

Domains Report
Print the number of the Wikipedia domains that have been updated, followed by a list of the domains sorted by the count of how many unique pages were updated on each. Pages with the same title are assumed to be the same.

Users Report
Print a list of users that have made changes to en.wikipedia.org domain, sorted by their total edit count (available as performer->user_edit_count in each event). If the same user shows up multiple times in the given time period, then use the highest edit count seen for them. Apart from regular users, various bots also make changes to Wikipedia pages. For generating this report, any bot users should be excluded. Whether a user is a bot or not is mentioned in the API response.

For your Reference:
Use the data provided by the https://stream.wikimedia.org/v2/stream/revision-create endpoint. This provides a real time feed of all the new revisions being created on Wikipedia.

To get started, you can find Javascript and Python example code and link to libraries here:
https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams

You can see the type of data you will receive from the API here:
https://stream.wikimedia.org/v2/ui/#/?streams=revision-create

