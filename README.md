# Project 31 Medical report analysis

## Installation/setup
1. Clone the repository
2. Apply for access to the Metathesaurus database, which can be found at https://www.nlm.nih.gov/research/umls/knowledge_sources/metathesaurus/index.html. My access was granted within a day.
3. Download the metathesaurus files, install MySQL server (version 5.5) and create a database called `metathesaurus` with utf-8 encoding.
4. Modify the metathesaurus .bat import scripts to use the correct database name and password. Then modify the tables script and replace all @LINE_TERMINATOR@ with \n.
5. Run the .bat import script. This will take many many hours to complete.
6. Install cTAKES https://ctakes.apache.org/downloads.cgi
7. Configure "config.py", and set the local subfolders for data collection, cTAKES output and parsing. Then set the cTAKES global /bin folder location, user agents for web scraping and UMls API key.
8. Set the number of reports in the config.py file. NOTE: More than 150 may trigger PubMed Central rate limiting, possibly resulting in an IP ban.
9. Pip install requirements.txt
10. Run the project31.ipynb file.