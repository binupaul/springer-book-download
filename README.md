# Springer Book Download

Python 3 script to download Springer books made available by Springer legally and free of charge.
This script uses the following libraries

* Beautiful Soup
* OpenPyXL
* Requests

The libraries are available from

* https://www.crummy.com/software/BeautifulSoup/
* https://openpyxl.readthedocs.io/en/stable/
* https://requests.readthedocs.io/en/master/

or can be downloaded via a package manager (apt)

* python3-bs4
* python3-openpyxl
* python3-requests

## Usage

First download the Excel sheet containing the list of books from here:

https://www.springernature.com/gp/librarians/news-events/all-news-articles/industry-news-initiatives/free-access-to-textbooks-for-institutions-affected-by-coronaviru/17855960

This script has been tested only with the English titles.

Springer has added a captcha check to prevent automated downloads (was not there before!). To bypass this, first download any book from the list manually from your browser and export the cookies files as a Netscape cookies.txt using a browser extension such as 'Export Cookies'.

```
usage: springer.py [-h] [--list | --topics] [--interactive] [--topic TOPIC]
                   [--isbn ISBN]
                   xlfile cookies

Download books from Springer

positional arguments:
  xlfile                the Excel file containing the book list
  cookies               the exported cookies file

optional arguments:
  -h, --help            show this help message and exit
  --list, -l            only list books
  --topics, -a          only list topics
  --interactive, -p     prompt for user input if required
  --topic TOPIC, -t TOPIC
                        use the given topic
  --isbn ISBN, -i ISBN  use the given ISBN

```

### Example

Download all Computer Science books

```
python3 springer.py --topic "Computer Science" Free+English+textbooks.xlsx cookies.txt

```
