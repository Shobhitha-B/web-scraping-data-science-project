"# web-scraping-data-science-project" 

Web scraping is a data extraction method that collects data only from websites.
It is often used for data mining and gathering valuable insights from large websites. 
Web scraping is also useful for personal use. Python includes a nice library called BeautifulSoup that enables web scraping. 
In this article, we will extract current stock prices using web scraping and save them in an excel file using Python.


Required Modules
The Requests module allows you to integrate your Python programs with web services.
The Beautiful Soup module is designed to make screen scraping a snap.
Using Python’s interactive console and these two libraries, we’ll walk through how to assemble a web page and work with the textual information available on it.
The Pandas module is designed to provide high-performance data manipulation in Python. 
It is used for data analysis that requires lots of processing, such as restructuring, cleaning or merging, etc.

Approach

Initially, we are going to import our required libraries.
Then we take the URL stored in our list.
We will feed the URL to our soup object which will then extract relevant information from the given URL based on the class id we provide it.
Store all the data in the Pandas Dataframe and save it to a CSV file.

Step 1: Import Libraries
We import the modules for Pandas, Requests, and Beautiful soup. 
Add a user agent and a header declaration. This makes sure that the target website for web scraping won’t automatically classify the traffic as spam and end up being blacklisted.
Many user agents are available at https://developers.whatismybrowser.com/

Step 2: Collect URLs to Scrap
We’ll assign the URL of the required stock web pages, www.groww.com in the list of URLs

Step 3: Retrieving Element Ids
We identify the element by looking at the rendered web page, but it’s impossible for a script to determine that. 
To find the target element, get its element ID and enter it into the script.

Step 4:  Try Data Extraction
Basically, during the extraction of data from a web page, we can expect AttributeError 
(When we try to access the Tag using BeautifulSoup from a website and that tag is not present on that website then BeautifulSoup always gives an AttributeError). 
To handle this error let’s use Try and except the concept.

     How does try() work? 

         First, the try clause is executed i.e. the code between the try and except clause.
        If there is no exception, then only the try clause will run, except the clause is finished.
        If any exception occurs, the try clause will be skipped and except clause will run.
        If any exception occurs, but the except clause within the code doesn’t handle it, it is passed on to the outer try statements. 
        If the exception is left unhandled, then the execution stops.
        A try statement can have more than one except clause. 

    We will use a list and store the company name, price of a stock, change in stock, and volume of each stock and store them in a list that consists of the stock data of all individual stocks.

Step 5: Storing Data to Data Frame 
Let’s declare the column names and using pandas create a Dataframe with columns: Company, Price, Change, and Volume.

        Next, we will iterate through the list and fill each data frame’s each row with the details of each company by using built-in functions loc( ).  The loc() function is label based data selecting method which means that we have to pass the name of the row or column which we want to select. The df.loc[index] = i, assigning the data to that row after that we will update the index in the Data Frame. The reset_index() is used to reset the index of the Data Frame from 0.






"# web-scraping-data-science-project" 
