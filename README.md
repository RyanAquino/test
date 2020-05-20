# Jira middleware
Server to replicate case from Jarvis to DCS Jira

Setup


The Following OS environment variables should be set:

> Set to ~/.bash_profile in Linux and unix base systems \
Set to System Properties > Environment Variables > User/System
```
> JIRA_TOKEN=<user:pass> - base64 encoded
> JIRA_URL=<URL of Jira instance>
> JARVIS_URL= <URL of Jarvis(Jira) instance>

> source ~/.bash_profile - reload environment variables
```

> To verify if set correctly
```
> echo $JIRA_URL
https://dcstaskcentral.trendmicro.com/jira/
```


> Note: Make sure you are running on a virtual environment

Creating Virtual Environment
```
> cd jira_middleware
> python -m venv venv
```

Install required packages
```
> pip install -r requirements.txt
```

Running a single test case
```
> python -m unittest tests\test_user_defined_request.py --verbose
```

Running all test cases
```
> python -m unittest discover --verbose
```
